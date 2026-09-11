# C(H)ORAL
## Sound becomes structure.

**A Green Shoe Garage Field Instrument · v1.0.0**

A multicolored, three-dimensional sculpture grown from sound. Recursive branches and a Life-inspired 3D cellular ecosystem influence one another. Music shapes subsequent growth and birth colors. Families, colonies, and persistent color mutations leave a history in the specimen.

**v1.0 incorporates Batch 7’s preservation/performance safeguards and the release validation pass.** This is a downloadable static release, not a deployment to a public website.

## Start here

Open **`index.html`**, or put it into a static hosting folder. The ZIP has that file at its root. It contains all JavaScript, shaders, CSS, icons, and interface markup: **no compilation, backend, account, CDN, external fonts, installation, telemetry, or runtime network dependencies**. The optional `src/`, `build.py`, and `tests/` are maintainer resources, not runtime requirements.

Select **Open music file** for your own music, or **Play test sound** for an audible test. Startup **Silent preview** is synthetic and clearly labeled; it is not listening. A browser with WebGL 2 is required.

**Before replacing an older HTML file, closing the tab, or upgrading, export the current specimen as JSON and confirm that it downloaded. Only settings autosave.** An image is not a resumable specimen, and browser warnings cannot protect against every forced close or crash.

## What changed in v1.0

| Area | Behavior |
| --- | --- |
| Portable exports | The complete snapshot is detached from the running simulation, validated for re-import, and given a CRC-32 accidental-corruption check before the download is initiated. |
| Import protection | Geometry, cells, birth records, ancestry, materials, settings, counters, and camera are validated before the open specimen is replaced. A confirmation summarizes the candidate. Cancel leaves both artwork and audio untouched. |
| Unsaved work | The specimen status is separate from settings autosave. Growth, material changes, and manual camera edits require another export. Seed and habitat changes warn before discarding unexported work. |
| Graphics recovery | A lost WebGL context pauses growth but retains the specimen in memory. JSON export still works. On restoration, GPU resources are rebuilt in place; the app never automatically reloads and discards the artwork. |
| Rendering budgets | Stationary Recorded views skip redundant drawing; live effects remain uniform-driven. Low quality limits halo work and samples fewer visible cells without deleting the simulation or desaturating its colors. |
| Diagnostics | Downloads contain environment/configuration categories and aggregate counts—not audio features, raw error messages, input filenames, seeds, geometry, birth records, or ancestry. |
| Compatibility | Actual VIVARIUM v0.1 and C(H)ORAL v0.2–v0.7 exports remain supported. No missing audio/color history is invented. |

## The creative workflow

**Sound → Habitat → Color → Grow → Save** are freely accessible sections, not a locked wizard. **Easy** exposes the everyday controls. **Advanced** reveals detailed audio, inheritance, palette, lighting, and cellular settings without resetting them.

Desktop uses a contained sidebar. Mobile uses a hideable bottom sheet. **Show controls / Hide controls** changes the space available to the sculpture. The main growth transport stays outside the panel.

### Sound

**Open music file** plays and analyzes a local audio file. The player has its own playback controls. The built-in test sound and **Advanced → Sound → Play color study** use real Web Audio analysis. Color study can hold 90 Hz bass, 1,000 Hz midrange, or 6,500 Hz treble, or cycle through those tones at five-second intervals.

**Microphone** and **Share tab / device audio** require explicit permission and suitable browser support. Capture needs HTTPS or localhost. A browser cannot automatically capture every sound on the device. The sharing dialog must provide an audio track; enable its audio option when available. Browser/OS/source restrictions still apply. The sharing API can require a video track, but C(H)ORAL does not display, record, or transmit it. Disconnect stops all acquired tracks.

Captured microphone or shared audio is not played back through your speakers by the app. Local file/test output can be muted independently from analysis. Source switching and disconnect release the previous stream and file URL. A failed or cancelled capture request leaves the existing source in place.

Bass influences extension, thickness, and available branching; mids influence organic branching; highs influence cellular mutation; loudness influences pace; transients can introduce new buds. These are artistic mappings, not instrument recognition, biological laws, or music transcription.

### Habitat

| Habitat | Growth family |
| --- | --- |
| Coral | Radial recursive reef |
| Dendrite | Upward branching canopy |
| Mycelium | Distributed spatial filaments |
| Crystal | Six-axis geometric recursion |
| Vortex | Helical branching |
| Tetra | Tetrahedral recursion |

Changing habitat starts a new specimen, with a warning for unexported work. Selecting the already active habitat does not reset it. **New seed**, **Same seed**, and a manually entered seed are deliberate reset operations.

### Color

**Full Spectrum is the default.** Reds, oranges, yellows, greens, blues, purples, and pinks coexist; this is not one object cycling through one hue. Reef, Aurora, Volcanic, Stained Glass, and Wild Type have different distributions, contrasts, aging, accents, and mutation policies. Original Biolume, Aurora, Ember, and Monochrome remain under Legacy. Monochrome remains intentionally neutral.

New growth records sound-feature summaries and its resulting birth color. A separate color random stream supports inheritance and mutation without changing the geometry random stream. Descendants can retain family colors; cells pass identities to branch buds and vice versa. The lineage legend shows the largest current cellular lineages. It is not an unlimited archive of extinct ancestors.

| Response mode | Current sound’s effect on the existing sculpture |
| --- | --- |
| Recorded | Shows stored material without live recoloring or animated accents. Subsequent growth can still record sound-composed colors. |
| Living | Temporarily shifts existing colors while retaining each material’s variation. Stored colors and ancestry are not overwritten. |
| Hybrid — default | Retains recorded body colors with localized live accents at tips, young cells, and spores. |

**Accent animation** governs localized highlights. In Living, disabling it does not disable the whole-body color response. Recorded and reduced motion suspend accents while retaining the selected preference. **Sound influence** affects subsequent birth colors and the strength of live effects, not a destructive repaint of recorded history.

**Restyle existing growth** applies the current palette and material controls to the whole view. **Affect new growth only** preserves the material currently on screen; subsequent palette/artist choices apply to new births. Surviving cells retain their material and carry it into dying spores. Mixed-palette appearances travel in the JSON.

**Color diversity, Sound influence, and Glow** are prominent. Advanced adds inheritance, mutation, lineage variation, smoothing, hue bias, saturation, and independent skeleton/cell/spore hue offsets. Material controls follow the selected color scope. Glow remains a global lighting effect.

### Lighting and 3D form

**Sculpture** provides neutral studio lighting and interior/underside fill. **Bioluminescent** emphasizes luminous cells and tips. **Unlit Color** displays unshaded material, preserving perspective and occlusion; it disables directional-light controls while leaving halos optional.

Surface illumination, self-emission, and halo intensity are separate. Direction, underside fill, and depth separation change the view without rewriting its material history. Selecting a treatment applies its starting settings. Individual edits show **Custom**. Resetting a treatment resets only its lights.

Halos are depth-tested against opaque geometry and sorted back to front. Their transparency is bounded rather than additively building to white. Spores fade through alpha while retaining their originating colors. Interface themes—dark, light, and high contrast—do not recolor the sculpture.

### Grow, move, and pause

Drag to orbit; wheel or pinch to zoom; right-drag or Shift-drag to pan. **Frame** restores a useful camera position. Keyboard focus on the canvas supports arrow orbit, +/− zoom, and Shift+arrow pan. Space pauses growth, B adds a Bloom, H toggles controls, and F frames the specimen.

**Pause growth** stops the simulation, not necessarily audio, auto-orbit, or live colors. **Still view** selects Reduced motion and pauses growth without muting audio or removing color. Motion preference offers **Follow device**, **Reduced**, and **Full motion**. Entering Reduced pauses growth and suppresses orbit, live effects, and interpolation. Leaving Reduced never silently resumes growth. Explicit Bloom and Resume remain available; manually resumed cellular changes are not motion-free.

Memory at **100 / Preserve** retains branches until reset or the structural cap. Lower memory settings deliberately retire older branches. Depth and branch settings affect subsequent growth, not an instant rebuild of existing geometry.

### Save and import

**Export specimen** saves JSON, including geometry, living cells, cell ages, growth substrate, queued growth tips, both random-generator states, birth colors and audio-feature summaries, color lineage identities, pending offspring traits, mixed materials, settings, continuation counters, and camera. It contains no raw audio or video. Import pauses growth and disconnects audio after confirmation; reconnect a source and resume deliberately.

Exports use stable `specimenSchema: 1`, chromatic schema 2, ecology schema 1, appearance schema 1, and continuation schema 1. The maximum portable file size is **64 MiB**, enforced on both import and export. The file does not preserve a music file, its playback position, a live analyser’s smoothing buffers, or an exact recording of prior sound. Exact simulation continuation requires the same subsequent input features and settings; replaying live music at a different time is not guaranteed to reproduce the same future.

The CRC-32 record checks accidental changes in the UTF-8 JSON payload. It is **not encryption, a digital signature, or evidence of authenticity**. Reformatting whitespace is safe. Editing or reordering payload properties changes the checksum. Older/unsigned developer documents are still structurally validated and clearly identified as lacking a checksum; do not remove a failed checksum from an important archive just to force it to load.

The status says **Export prepared**, not “saved to disk”: confirm the browser download. Further growth or material/manual-camera changes mark it unexported again. Automatic orbit alone does not continuously invalidate the export. A PNG captures the currently displayed sculpture, not the complete page, sound, or living state. PNG export does not clear the specimen’s unsaved status.

Files are parsed and validated into a candidate before replacement. Malformed files do not disconnect audio or move the camera. Confirmation lists the source version, generation, branch/cell counts, and available history. Cancellation does not alter the open work. Concurrent or superseded file reads cannot replace a specimen reset while the file was being read.

Legacy v0.1/v0.2 materials use their original/reconstructed color formulas; no past audio features are fabricated. v0.3 birth colors are retained, with no invented earlier ancestry. Later ancestry, lighting, and mixed-material archives remain intact where recorded. The receiving device’s theme, complexity, and motion preferences take precedence over imported local preferences. Current-format malformed settings/camera are rejected rather than silently clamped.

Only settings autosave into `gsg.choral.settings.v1`. Accessible legacy `gsg.vivarium.settings.v1` settings migrate without deleting or overwriting that key. Damaged settings are backed up to a recovery key when storage permits. Origin storage may be unavailable, and one origin cannot read another origin’s settings. JSON is the portable route between sites/devices. **Fresh start** clears the current sculpture and C(H)ORAL settings after confirmation; it is not a backup operation.

## Performance and limits

The cellular grid is **32 × 32 × 32**, with synchronous updates, 26 neighbors, and fixed empty boundaries. New births are constrained to the deposited growth substrate. This is a custom Life-inspired 3D ecosystem with explicit randomness—not classic 2D Conway Life or a biological model.

| Quality | Future branch cap | Approximate visible-cell target | Maximum rendered halos | Dynamic draw target |
| --- | ---: | ---: | ---: | ---: |
| Low | 5,500 | 3,200 | 500 | Up to 24 frames/s |
| Balanced | 10,000 | 6,000 | 1,800 | Up to 40 frames/s |
| High | 16,000 | 11,000 | 4,500 | Up to 60 frames/s |

These are **work budgets, not measured performance guarantees**. All cells remain simulated; only visible cells/halos are sampled. Lowering quality preserves existing branches even above the lower cap but prevents new ones until capacity is available. Cell sampling is spatially distributed and approximate; it does not keep only a central plane or a single colony. Geometry updates and manual edits can trigger immediate drawing outside the normal live cadence. Static Recorded views with orbit off skip redundant draws. Hidden-page rendering is skipped. Color variation is not reduced to improve speed.

The instrument remains finite. It is not unlimited-growth software, a persistent cloud service, an installable service-worker PWA, an audio recorder, or a video exporter. The downloaded HTML is offline-capable without runtime network requests; loading it from a site still needs that page to be available unless you keep a local copy.

## Validation and release status

See **[VALIDATION.md](VALIDATION.md)** for executed counts, matrices, actual downloads, compatibility fixtures, environment, and limitations. Tests use the shipped application and renderer, not generated mockups. A static ZIP is delivered; no public site was deployed.

Normal hosted-origin navigation/storage testing is blocked by the managed validation browser’s policy and is reported as blocked, not passed. Hardware microphone/system capture, actual target-host storage, OS Save/permission dialogs, real-GPU performance, long mobile sessions, and assistive-technology review remain target-device checks. Browser-level downloads are tested separately where available.

## Maintainers

Editing the delivered `index.html` directly is possible. To regenerate it from optional source files:

```sh
python3 build.py
```

To run the validation suites in a suitable development environment:

```sh
python3 tests/run_validation.py
```

Development tests require Node.js, Python, Playwright, Pillow, numpy, Chromium, and Xvfb. None is required to use the application. `SHA256SUMS` covers the packaged files except the manifest itself. Tests and examples use synthetic signals and contain no captured user audio.

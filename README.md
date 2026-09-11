# C(H)ORAL
## Sound becomes structure.

**A Green Shoe Garage Field Instrument — v0.7.0 — Batch 6**

A multicolored, three-dimensional sculpture grown from sound. Recursive branches and a Life-inspired cellular ecosystem influence one another. Audio shapes subsequent growth and birth colors; families, colonies, and color mutations leave a history in the specimen.

**Batch 6 adds a five-step creative workspace, Easy/Advanced controls, Recorded / Living / Hybrid color response, independent accent animation, and device-aware reduced motion.** This release is a local static package, not a website deployment.

## Open or host it

Open **`index.html`** in a browser with WebGL 2 available, or place it in a static hosting folder. The ZIP has `index.html` at its root. The delivered HTML contains all JavaScript, shaders, CSS, and interface assets. No build step, installation, account, backend, CDN, remote fonts, telemetry, or runtime network dependencies are required. The `src/` files and `build.py` are optional maintainer resources.

**Export the current specimen before closing, reloading, or upgrading. Only settings autosave—not the growing sculpture.** Existing saved settings should not be cleared just to install this release.

Capture features require an appropriate secure browser context, explicit permission, and an available audio track. Audio sharing availability differs by browser, operating system, and selected source. C(H)ORAL cannot silently listen to every sound playing on a device. Test microphone/system sharing on the intended device. A local music file and the audible test sound provide alternative inputs.

## First session

1. **Sound:** choose **Open music file** or **Play test sound**. Startup uses **Silent preview**, explicitly synthetic and not listening.
2. **Habitat:** choose Coral, Dendrite, Mycelium, Crystal, Vortex, or Tetra. Changing habitat starts a new specimen. The current habitat button is a no-op; use New seed to restart deliberately.
3. **Color:** keep Full Spectrum, or choose another palette. Select Recorded, Living, or Hybrid. Adjust Color diversity, Sound influence, and Glow.
4. **Grow:** adjust Growth intensity, pause/resume, add a Bloom, choose visible layers, or change movement preferences. The main transport stays available outside the panel.
5. **Save:** export the living specimen as JSON or save the rendered view as a PNG.

The steps are shortcuts, not a locked wizard: jump freely between them. **Easy** starts with everyday controls. **Advanced** reveals detailed audio, ancestry, palette, lighting, and cellular rules in their relevant step. Switching complexity never resets values or silently lowers simulation quality.

Desktop controls occupy a contained sidebar, leaving the sculpture dominant. Phones use a bottom sheet that can be hidden with **Hide controls**. Its header and navigation stay available while the selected step scrolls. Controls start hidden on small screens; press **Show controls**. Interface theme remains independent of the artwork palette.

## Three color-response modes

| Mode | What current sound does to the existing sculpture |
| --- | --- |
| **Recorded** | No live recoloring, localized accents, or audio-driven emission pulses. The current material treatment and its growth history remain visible. New growth still records sound-composed colors. |
| **Living** | Temporarily shifts the hue of existing branches, cells, and spores according to smoothed audio. Each material retains its own color variation, saturation, and brightness; the whole sculpture does not become one uniform RGB. |
| **Hybrid — default** | Retains the recorded body treatment while allowing localized live highlights on young tips, young cells, and selected spores. |

These are **view modes**, not destructive edits. They do not rewrite geometry, birth colors, audio-feature records, ancestry, appearance archives, pending offspring, or random-generator state. Switching from Living to Recorded restores the underlying material treatment. The audio connection and camera are not reset.

Living is intentionally an artistic hue-rotation layer. It does not recognize musical instruments or infer scientifically inherent sound/color correspondences. Bass-dominant, midrange-dominant, and treble-dominant signals favor different rotations, with the smoothed mixture and energy controlling the result. Silence returns the live layer to the underlying material. Recorded material can still mature or be deliberately restyled; Recorded does not freeze simulation age or override the palette controls.

### Accent animation is separate

**Accent animation**, in Color, controls localized highlights. In Living, turning it off leaves the whole-body color response active. In Hybrid, turning it off leaves the recorded material without live accents. Recorded and reduced motion disable the checkbox, explain why, and preserve its chosen value for later use.

**Sound influence** scales new birth-color composition and the live response. Zero removes live hue shifts and localized sound effects; it does not erase earlier birth records. Glow controls halos, not body illumination.

**Pause growth** stops the simulation, not audio playback or all visual motion. A paused specimen can still respond in Living or Hybrid and can still auto-orbit. Use **Still view** to stop all automatic visual movement.

### Compare the modes

In Color, select Full Spectrum. In Grow, disable Auto orbit and pause growth so the camera and geometry stay fixed. In Advanced → Sound → **Audio study & input tuning**, choose a sustained tone or the five-second cycle, then press **Play color study**.

Compare Recorded, Living, and Hybrid in Color. Living should recolor existing material as the tone changes. Recorded should not. Hybrid limits live effects to localized accents; very mature branch bodies deliberately respond less. To inspect only stored material, select Recorded or Still view.

## Motion and comfort

**Grow → Motion** offers:

| Preference | Behavior |
| --- | --- |
| **Follow device — default** | Reads the device’s current reduced-motion preference and reacts to changes during the session. An older saved `motion: true` does not override a current device request for reduced motion. |
| **Reduced** | Suspends auto-orbit, live recoloring, localized accents, emission pulses, and growth interpolation. Rich stored colors, palette selection, lighting controls, and manual camera operation remain available. |
| **Full motion** | An explicit override of the device preference. Auto orbit and accent animation still have independent controls. |

Entering reduced motion pauses growth. Leaving it **does not automatically resume growth**. The user can explicitly Resume or Bloom in Reduced mode; generations then update without interpolation. This is not a promise that resumed cellular changes are motion-free. The audio analyser and playback may continue.

**Still view**, in the desktop header and in Grow on every layout, pauses growth and selects Reduced. It does not mute playback, change the palette, or erase colors. To reenable live effects, choose Follow device or Full motion in Grow; resume growth separately as needed.

The reduced interface suppresses spectrum/meter motion, onset indicators, animated color chips, and CSS transitions. Numeric analysis is updated less frequently. An older master-animation-off setting migrates to Reduced. A fresh installation follows the device dynamically rather than storing a permanent forced-off setting.

## Six palettes and preserved material

Full Spectrum, Reef, Aurora, Volcanic, Stained Glass, and Wild Type have different distributions, accents, aging, variation, and mutation rules. Use **Browse palette previews** to see their swatches. The selector also retains the original Biolume, Aurora, Ember, and Monochrome formulas under Legacy. The original Aurora is not replaced by the new Aurora treatment.

**Color → Where color changes apply** separates:

- **Restyle existing growth:** deliberately apply current palette/diversity/hue/saturation to existing and subsequent material, without changing canonical birth history.
- **Affect new growth only:** freeze the material treatment currently displayed; later material choices affect subsequent births. Surviving cells retain their treatment, and dying cells pass it into spores.

**Living is a temporary overlay even in new-growth-only scope.** Scope preserves material, not a past lighting environment or frozen live animation. Return to Recorded to inspect each preserved material without that overlay. Mixed-palette treatment travels in the specimen export.

Advanced reveals saturation, global hue bias, independent skeleton/cell/spore hue offsets, color inheritance, mutation, lineage variation, color smoothing, ancestry counts, and the colony legend. All existing functions remain present; none is silently reset by Easy mode.

## Lighting retained from Batch 5

**Color → Lighting treatments** opens the lighting section and focuses its treatment selector. Sculpture uses neutral studio light with visible underside fill. Bioluminescent emphasizes luminous cells and tips. Unlit Color shows material without directional shading, emission, or depth dimming; halos remain optional.

Advanced reveals separate Surface illumination, Self-emission, Interior / underside fill, light direction, and Depth separation. Glow remains in the main Color controls and changes halos/spores only. Selecting a treatment applies its starting lighting controls. Reset this treatment does not reset palette, appearance scope, camera, audio, or geometry. Inapplicable surface controls are disabled in Unlit Color.

Halos are depth-tested against opaque geometry, sorted back-to-front, and composited with bounded premultiplied transparency. Aging spores retain RGB while fading opacity. Lighting is an artistic renderer, not volumetric or physically based light transport.

In this release **interface theme no longer changes halo strength**. Canvas RGBA output is the same for light, dark, and high-contrast interface themes at otherwise identical settings. A different background can still affect perceived contrast.

## Explore in three dimensions

Drag to orbit; scroll or pinch to zoom. Right-drag or Shift-drag to pan. Frame resets framing; zoom extends well outside the specimen. The panel changes the projection’s framing offset without rewriting camera state.

Focus the scene for keyboard operation: arrow keys orbit, Shift + arrows pan, plus/minus zoom. **F** frames, **Space** pauses/resumes growth, **B** adds a Bloom, and **H** toggles controls. **Escape** closes the field guide or controls. Hiding a panel containing focus returns focus to its toggle. Form controls retain native keyboard behavior; the color-response group uses native radios.

Auto orbit is in Grow. Manual camera navigation remains available in Reduced mode.

## Save, import, and compatibility

**Export specimen** prepares a JSON containing living state, branch geometry, canonical birth colors, source-tagged audio-feature summaries, color lineages, pending offspring traits, separate color RNG state, mixed-material appearance, settings, and camera. It does not contain the audio itself or reconstruct a song.

**Save PNG** prepares only the current 3D canvas with a transparent background, not the interface. The Save step reports the generation at which an export was prepared. This is not confirmation that the native browser download was retained on disk. Subsequent growth is not automatically included in an earlier export.

Imports are validated before replacing the open specimen, disconnect audio, and pause growth. Versions supported: original VIVARIUM v0.1 and C(H)ORAL v0.2 through v0.7. Older data retains the history it actually recorded; absent audio or ancestry is never fabricated. Current-format malformed response/motion/lighting fields are rejected transactionally rather than quietly replaced.

Imports adopt the specimen’s artistic choices, including color-response mode and lighting. They **retain this device’s current interface theme, Easy/Advanced choice, and motion preference**, instead of imposing another person’s accessibility choices. Engine-level round trips preserve all settings; the UI applies this explicit local-preference policy on import.

Settings remain in `gsg.choral.settings.v1`. Accessible legacy settings from `gsg.vivarium.settings.v1` are copied without deleting or changing the old key. Corrupt settings are backed up to a recovery key when storage permits. Cross-origin storage cannot be migrated automatically; use specimen export/import. File-origin and private-browser storage behavior needs testing on the actual device.

## Boundaries and privacy

The ecosystem is a bounded, experimental 3D Life-inspired automaton with 26 neighbors, fixed empty boundaries, explicit mutation, substrate-limited births, branch seeding, and occasional low-population reseeding—not classic two-dimensional Conway’s Life or a biological model.

The 32³ cellular volume is finite. Geometry budgets bound rendered detail and branch growth; the high-detail branch cap is 16,000. A cap preserves prior structure rather than silently deleting it. Structural memory below 100 deliberately retires older branches. Same seeds reproduce initial conditions; live sound and timing can change subsequent growth. This release does not offer unlimited growth, audio transcription, a full historical genealogy, or exact-song replay.

No audio, specimen, diagnostic, or usage information is uploaded. Microphone input is not played through the speakers by default. Audio sharing can require a video track, but C(H)ORAL does not render, store, record, or transmit it; capture tracks stop when disconnected. Diagnostics contain settings, counters, summarized signal values, and errors, not raw audio or specimen geometry. Review a diagnostic export before sharing it.

## Validation and maintainer files

See **VALIDATION.md** for executed checks, artifacts, environment details, and explicit limitations. Browser tests use Chromium with software WebGL. Test-only Node/Python/Playwright dependencies are not needed by the application.

```sh
python3 build.py
python3 tests/run_validation.py
```

The builder assembles the checked-in source into the already-provided standalone `index.html`. Source modules retain the original simulation and color systems; `response.js` supplies view-only response/motion policy, and `workspace.css` supplies the new workspace layout.

Hardware microphone/system capture, native permission/save/fullscreen dialogs, durable intended-host storage, real-GPU performance, and long sessions still require device-level checks. **No website was deployed.**

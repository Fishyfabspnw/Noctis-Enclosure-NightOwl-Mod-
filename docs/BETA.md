# Beta status — v0.1.0-beta.1

Released 2026-08-30 for CAD review, modification, and feedback. **Adjustments are still required.** This is not a production-ready or fully validated build release.

## Confirmed export findings

- Complete Fusion assembly exported to STEP AP214 with invisible components and bodies included.
- FreeCAD 1.0.1 / Open CASCADE recovered **3,345 solids**, matching the source's solid-instance count.
- **Two solids fail Open CASCADE validity checking.** Face counts and centers of mass identify `Body1` in the two `LDO-36STH17-1004AHG` motor reference components under `MMU PARTS > Dual Nightwatch > Hardware > Motion`. They were preserved, not repaired or removed. The STEP must not be described as passing all geometry checks.
- **Four hidden bodies are included:** one extrusion body and three bodies under mirrored radial-fan components. One hidden fan body is away from the main enclosure on the negative Y side and may cause a wide zoom-to-fit. Other hidden fan geometry can overlap visible geometry. The [inventory](../CAD/assembly-inventory.json) records original visibility.
- Product geometry was not redesigned as part of this export/rendering release.

The source-visible assembly is approximately **227.9 × 499.2 × 386.5 mm** along Fusion's X/Y/Z axes; Y is vertical. These are approximate orientation bounds, not fabrication dimensions. Full-export bounds differ because of hidden geometry. Open CASCADE's analytic bounding box also overestimates some curved geometry; the [validation report](../CAD/export-validation.json) separates analytic and tessellated bounds.

## Still needs review

These are **validation tasks**, not a claim that every listed area has a confirmed defect:

- [ ] Review/repair motor reference-body validity failures as needed for downstream CAD use.
- [ ] Decide which hidden extrusion/fan bodies belong in a future cleaned release; resolve the off-assembly fan placement.
- [ ] Check panel sizing, hole alignment, door clearances, hinges, and hardware access.
- [ ] Check printed-part tolerances, fastener lengths, inserts, and assembly clearances.
- [ ] Verify spool/rewinder travel, Dual Nightwatch access, and PTFE routing.
- [ ] Check dryer mounting, fan/blower placement, airflow, and component temperature limits.
- [ ] Validate electrical integration, control behavior, and appropriate thermal protection before heated operation.
- [ ] Verify LED/sensor mounting and wire routing against the intended electronics.
- [ ] Publish a tested Noctis-specific BOM, print orientations/settings, and assembly instructions.
- [ ] Publish a complete native Fusion source package with external dependencies; this beta includes STEP geometry, not the editable Fusion timeline.
- [ ] Record operating results and resolve fit issues before a stable release.

The old README's 45–65°C range was not supported by test evidence in this repository. This beta makes **no verified temperature, drying, or thermal-safety performance claim**. Renderings are presentation images, not evidence of validation.

## Report an adjustment

[Open an issue](https://github.com/Fishyfabspnw/Noctis-Enclosure-NightOwl-Mod-/issues/new/choose) with the release tag, CAD application/version, component/body name, screenshots, expected versus observed fit, measurements, and applicable print settings. Mark proposed changes as tested or untested.

The original [NightOwl documentation](https://github.com/mjonuschat/NightOwl) is background information, not a verified build guide for this modified enclosure.

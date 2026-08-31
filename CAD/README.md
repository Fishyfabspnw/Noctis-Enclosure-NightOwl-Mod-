# Noctis beta CAD — v0.1.0-beta.1

## Complete assembly

[`Noctis-NightOwl-v0.1.0-beta.1.step`](Noctis-NightOwl-v0.1.0-beta.1.step) is the entire active Fusion root assembly exported on 2026-08-30, including invisible components and bodies. It is STEP AP214 with **millimeter** length units, approximately 89.7 MB (85.5 MiB).

The source was the in-memory `NIGHTOWL ENCLOSURE` document, based on cloud version 14 with pending changes. Exporting did not save or overwrite that document. The 12 top-level groups cover feet, panels/door, MCU mounts, printed covers, extrusions, skirts, MMU parts, dryer, fans, PTFE guides, LEDs, and blower modifications.

The STEP contains **3,345 solid instances** across **1,445 source component occurrences**. Hardware and reference bodies are included; this is not an isolated set of printable parts. STEP is editable geometry and assembly data, not a native Fusion feature timeline.

## Import findings

FreeCAD 1.0.1 / Open CASCADE successfully reads the file and recovers all 3,345 solids. **Two motor reference solids fail its validity check.** This is a successful import/count check, not a clean bill of geometric health or a fabrication approval.

The source contained four hidden bodies. They are included so this is a complete export, but a receiving application may show them. One hidden mirrored fan body is away from the main assembly and can make zoom-to-fit look wrong. Hide that body for assembly viewing; do not assume it marks the enclosure's outside dimensions.

- [Source assembly inventory](assembly-inventory.json): body names, component paths, visibility, and solid flags.
- [Export validation](export-validation.json): checks, counts, dimensions, and diagnostic results.
- [Beta notes](../docs/BETA.md): known limitations and review checklist.
- [SHA-256 checksums](SHA256SUMS.txt): STEP download integrity.

Open CASCADE's analytic bounding box overestimates some curved geometry. The validation JSON also records bounds from a 0.2 mm tessellation; those include the hidden displaced fan. Neither set is a fabrication drawing.

## Native source limitation

A complete Fusion source package is not included in this beta. The tested local F3D export contains external references and cannot open as a standalone design. Fusion's F3Z export would first save pending cloud changes, which was not performed during this STEP-export task. The incomplete F3D is not published as a usable download. A complete native package remains on the beta checklist.

## Download and open

Use the [release assets](https://github.com/Fishyfabspnw/Noctis-Enclosure-NightOwl-Mod-/releases/tag/v0.1.0-beta.1) or the raw STEP download. GitHub may not display a preview because of the file's size. Import it in a STEP-capable CAD application, confirm millimeter units, and review hidden/reference parts before editing or extracting printable geometry.

Retain [NightOwl attribution](../ATTRIBUTION.md) and the applicable [GPL-3.0 license](../LICENSE) with derivatives.

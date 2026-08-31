# Noctis — NightOwl Enclosure Mod

**A community modification of [NightOwl by mjonuschat](https://github.com/mjonuschat/NightOwl), maintained by [FishyFabsPNW](https://github.com/Fishyfabspnw).**

Noctis adapts the NightOwl dual-spool filament switching system into an enclosed, dryer-assisted filament and MMU assembly. It retains the original project's foundations while adding enclosure panels and a door, dryer integration, circulation, PTFE guides, and LED-related parts.

> **BETA — v0.1.0-beta.1**
> This is a work-in-progress CAD release for review, modification, and testing. Some parts still need adjustment. Fit, routing, thermal performance, and the complete build process are not validated by this release. Read the [beta notes](docs/BETA.md) before printing or buying parts.

![Noctis beta assembly, front three-quarter studio rendering](renders/01-front-three-quarter.png)

## Download the beta

**[Beta release and downloads](https://github.com/Fishyfabspnw/Noctis-Enclosure-NightOwl-Mod-/releases/tag/v0.1.0-beta.1)** · **[Complete STEP file](https://github.com/Fishyfabspnw/Noctis-Enclosure-NightOwl-Mod-/raw/refs/heads/main/CAD/Noctis-NightOwl-v0.1.0-beta.1.step)**

| File | Purpose |
| --- | --- |
| [`Noctis-NightOwl-v0.1.0-beta.1.step`](CAD/Noctis-NightOwl-v0.1.0-beta.1.step) | Complete assembly, including hidden bodies/components. STEP AP214; millimeter units. |
| [CAD export notes](CAD/README.md) | Export scope, import checks, hidden geometry, and checksums. |

The full STEP includes hardware and reference parts; it is **not** a ready-to-print part pack. Four hidden bodies are intentionally retained, including an off-assembly mirrored fan body that can affect zoom-to-fit. The [assembly inventory](CAD/assembly-inventory.json) records source visibility. STEP is editable CAD geometry but does not retain Fusion's feature history; a complete native Fusion package is not included in this beta.

## What Noctis adds

- Panel-and-door enclosure around the filament and MMU assembly.
- Dryer mounting and a PolyDryer-based integration concept.
- Chamber fans and blower-related parts.
- PTFE guide and LED-related parts.
- Revised covers, skirts, feet, and MCU mounting arrangements.

These describe the CAD snapshot and design intent, not completed performance testing. The earlier README's 45–65°C wording should not be treated as a verified operating range. Noctis is a filament/MMU enclosure; this release does not establish a heated printer build-chamber specification.

## Render gallery

Six views rendered from the actual beta CAD, with soft studio lighting and a dark blue-gray reflective background matched to the earlier GitHub renderings. Presentation materials and transparency are adjusted for readability. These are CAD renderings, not photographs or proof of a tested build.

| Front three-quarter | Opposite three-quarter |
| --- | --- |
| ![Front three-quarter](renders/01-front-three-quarter.png) | ![Opposite three-quarter](renders/02-opposite-three-quarter.png) |

| Rear three-quarter | Front elevation |
| --- | --- |
| ![Rear three-quarter](renders/03-rear-three-quarter.png) | ![Front elevation](renders/04-front-elevation.png) |

| Dryer and top mounting | Lower MMU and skirts |
| --- | --- |
| ![Dryer detail](renders/05-dryer-detail.png) | ![MMU detail](renders/06-mmu-detail.png) |

[Full-resolution gallery and rendering notes](renders/README.md) · [Earlier project images](docs/LEGACY-IMAGES.md)

## Original project and credits

**The original NightOwl design is by [mjonuschat](https://github.com/mjonuschat/NightOwl). Noctis is a derivative community mod, not an official NightOwl release.** No affiliation or endorsement is implied.

Start with the upstream [NightOwl documentation](https://github.com/mjonuschat/NightOwl), [bill of materials](https://github.com/mjonuschat/NightOwl/blob/main/BOM.md), and [assembly manual](https://github.com/mjonuschat/NightOwl/blob/main/Manual/NightOwl%20Assembly%20Manual.pdf) for the original system. Those instructions and quantities are not a verified Noctis build guide or BOM.

This project also acknowledges:

- Hartk's [Dual Nightwatch](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch) and [Bowden Y-Splitter](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Extruders/Dual_Nightwatch/STLs/Bowden_Y).
- The Enraged Rabbit Community's [Filamentalist Rewinder](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder).
- BIGTREETECH's [MMB controller project](https://github.com/bigtreetech/MMB).
- ArmoredTurtle's [TurtleNeck](https://github.com/ArmoredTurtle/TurtleNeck).

See [ATTRIBUTION.md](ATTRIBUTION.md) for the modification notice, provenance limits, and third-party notices.

## Feedback and license

Found a fit issue, interference, routing problem, or import error? [Open an issue](https://github.com/Fishyfabspnw/Noctis-Enclosure-NightOwl-Mod-/issues/new/choose) with the version, component name, screenshots, and measurements. The [beta checklist](docs/BETA.md) lists areas needing review.

This NightOwl-derived work is distributed under the **GNU General Public License v3.0**, consistent with upstream. The full upstream license text is included in [LICENSE](LICENSE). Third-party projects and commercial hardware references retain their respective notices and applicable terms. See the [changelog](CHANGELOG.md).

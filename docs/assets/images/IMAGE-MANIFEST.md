# Image Placement Manifest

Generated from the source PDFs in "Documentation dump (BOSS) 2". Every image below was extracted directly from its source PDF and placed on its matching page inside the corresponding markdown file. No images came from any external source.

| Source PDF | Markdown file | Images placed | Unmatched (approximate placement) | Repeated logos deduped |
|---|---|---|---|---|
| CE Express User Guide v7.3.pdf | `docs/ce-express/user-guide/user-guide-v7.3.md` | 509 | 1 | 6 |
| 01. CE Express. Creating Workspace.pdf | `docs/ce-express/training/01-creating-workspace.md` | 25 | 1 | 0 |
| 02. CE Express. Create Objects.pdf | `docs/ce-express/training/02-create-objects.md` | 32 | 3 | 0 |
| 03. CE Express. Line Of Sight (Profile).pdf | `docs/ce-express/training/03-line-of-sight.md` | 29 | 1 | 0 |
| 04. CE Express. RF Prediction.pdf | `docs/ce-express/training/04-rf-prediction.md` | 45 | 1 | 0 |
| 05. CE Express. Import data.pdf | `docs/ce-express/training/05-import-data.md` | 19 | 2 | 0 |
| 06. CE Express. Prediction models.pdf | `docs/ce-express/training/06-prediction-models.md` | 30 | 1 | 0 |
| 07. MW Equipment.pdf | `docs/ce-express/training/07-mw-equipment.md` | 33 | 1 | 0 |
| 08. MW Prediction.pdf | `docs/ce-express/training/08-mw-prediction.md` | 32 | 1 | 2 |
| 09. Preparing Geodata.pdf | `docs/ce-express/training/09-preparing-geodata.md` | 21 | 1 | 0 |
| CE Express Administrator Guide v7.2.pdf | `docs/ce-express/user-guide/admin-guide-v7.2.md` | 129 | 1 | 1 |
| CE Express only Administrator Guide v7.2.pdf | `docs/ce-express/user-guide/admin-guide-only-v7.2.md` | 73 | 1 | 1 |
| 0. Software installation and upgrades.pdf | `docs/ce-pro/training/00-installation.md` | 19 | 5 ⚠️ | 2 |
| 00. Data types.pdf | `docs/ce-pro/training/01-data-types.md` | 56 | 10 ⚠️ | 5 |
| 000. Architecture.pdf | `docs/ce-pro/training/02-architecture.md` | 52 | 13 ⚠️ | 4 |
| 0000. Agenda.pdf | `docs/ce-pro/training/03-agenda.md` | 5 | 1 ⚠️ | 2 |
| 1. Creating Workspace.pdf | `docs/ce-pro/training/04-workspace.md` | 27 | 10 ⚠️ | 2 |
| 2. Line of Sight (Profile).pdf | `docs/ce-pro/training/05-line-of-sight.md` | 60 | 18 ⚠️ | 5 |
| 3. Creating objects.pdf | `docs/ce-pro/training/06-objects.md` | 18 | 6 ⚠️ | 2 |
| 4. Cell prediction.pdf | `docs/ce-pro/training/07-cell-prediction.md` | 18 | 6 ⚠️ | 2 |
| 5. Prediction models.pdf | `docs/ce-pro/training/08-prediction-models.md` | 42 | 14 ⚠️ | 32 |
| 6. Importing data.pdf | `docs/ce-pro/training/09-importing-data.md` | 19 | 5 ⚠️ | 2 |
| 7. RL Prediction.pdf | `docs/ce-pro/training/10-rl-prediction.md` | 30 | 14 ⚠️ | 2 |
| Inventory3D User Guide v4.6.pdf | `docs/inventory3d/user-guide.md` | 153 | 2 | 1 |
| Cellular Expert Geodata Requirements 2025.pdf | `docs/geodata/geodata-requirements.md` | 24 | 1 | 2 |
| Requirements for CE Network Objects.pdf | `docs/geodata/network-objects-requirements.md` | 6 | 0 | 0 |
| CE Desktop RCP for ArcGIS Pro User Guide v4.9.pdf | `docs/ce-pro/rcp-user-guide.md` | 339 | 8 | 11 |
| CE Desktop RLP for ArcGIS Pro User Guide v4.9.pdf | `docs/ce-pro/rlp-user-guide.md` | 317 | 4 | 7 |
| CE Desktop EMF for ArcGIS Pro User Guide v4.9.pdf | `docs/ce-pro/emf-user-guide.md` | 233 | 3 | 6 |
| CE Desktop Indoor for ArcGIS Pro User Guide v4.9.pdf | `docs/ce-pro/indoor-user-guide.md` | 238 | 3 | 6 |
| CE Desktop Sound for ArcGIS Pro User Guide v4.9.pdf | `docs/ce-pro/sound-user-guide.md` | 231 | 3 | 6 |

**Totals: 2864 images placed, 141 (4.9%) with approximate rather than confirmed placement, 109 repeated logo/watermark images deduped (kept once each in a `repeated/` subfolder instead of duplicated on every page).**

⚠️ = flagged for manual review (over 15% of that document's images could not be matched to a confirmed page anchor and were placed sequentially near their expected position instead).

Flagged files are concentrated in `docs/ce-pro/training/00-installation.md` through `10-rl-prediction.md` — these 11 files appear to have been rewritten/summarized during the original PDF-to-markdown conversion rather than kept close to the source wording, so exact per-image anchoring is inherently less reliable there. All other documents matched at 95%+ confidence.

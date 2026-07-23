# Cellular Expert Documentation

Source content for Cellular Expert's product documentation: **CE Express**, **CE Pro**, **Inventory3D**, plus supporting geodata requirement docs. All content is converted from the original PDF user guides / training manuals into markdown.

## Image convention

Every screenshot/icon lives under `docs/assets/images/<product>/<guide-name>/`, named `pNNN-imgM.png` (page NNN, image M on that page). Markdown pages reference them with a relative path:

```markdown
![Image p255](../../../assets/images/ce-express/user-guide-v73/p255-img1.png)
```

Small inline button icons (the kind that appear mid-sentence, e.g. "Click this button [icon] to open the tool") use the literal alt text `icon` instead of a description. This is a signal the front-end (CellularExpertPortal) picks up on to render the image small and inline rather than as a full-width block:

```markdown
Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p255-img1.png) to open the tool.
```

## Known gaps

- **CE Express** (`docs/ce-express/user-guide/v73-sections/`) has been manually verified page-by-page against the source PDF — image placement, section splitting, and content should match the PDF exactly.
- **CE Pro's 5 user guides** had images auto-placed by an extraction pipeline (see `docs/assets/images/IMAGE-MANIFEST.md` for per-file placement counts) but have **not** been manually spot-checked against the PDFs yet.
- **CE Pro's training docs** are flagged in the manifest as the weakest spot — several have 15%+ of pages where the auto-placement pipeline couldn't confidently match an image to its page, so those are more likely to have misplaced or missing images.
- Raw source PDFs for CE Pro (`docs/ce-pro/user-guide-pdf/`, `docs/ce-pro/training-pdf/`) are kept as a reliable fallback alongside the markdown versions.

## Two deployment paths (worth knowing about)

This repo currently feeds two different viewers, and they are not in sync:

1. **CellularExpertPortal** (separate repo, custom React app) — reads directly from this repo's `pooja` branch and is what's been actively worked on and previewed via `npm start`. This is where the CE Express per-section split is actually used.
2. **`mkdocs.yml` + GitHub Pages** — a GitHub Action rebuilds and deploys a separate MkDocs Material site whenever `main` is pushed to. Its nav still points at the old single-file docs, not the new per-section split, and only picks up changes pushed to `main` (not `pooja`).

If the MkDocs/GitHub Pages site is meant to reflect the same fixes as the Portal, `mkdocs.yml`'s nav needs updating, and those changes need to reach `main`.

## Running the viewer locally

The docs themselves aren't runnable — pair this repo with **CellularExpertPortal**:

```
cd CellularExpertPortal
npm start
```

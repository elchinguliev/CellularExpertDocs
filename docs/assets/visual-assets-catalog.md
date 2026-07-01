# Visual Assets Catalog

This file catalogues all visual assets (screenshots and icons) to be stored in the PostgreSQL database and integrated into CE documentation.

- **CE Pro docs** → ArcGIS Pro screenshots (CE Pro runs inside ArcGIS Pro, so these match directly)
- **CE Express docs** → Esri Calcite SVG icons (CE Express is a web app; real screenshots must be taken from the live CE Express application — see notes below)

**Icon source:** [Esri Calcite UI Icons](https://github.com/Esri/calcite-ui-icons) (open-source, Esri official)
**Screenshot source:** [ArcGIS Pro documentation](https://doc.esri.com/en/arcgis-pro/latest/get-started/get-started.html) (Esri official)

> ⚠️ **CE Express screenshots** — The entries marked `[SCREENSHOT NEEDED]` require a real screenshot taken from the running CE Express web application. These cannot be sourced from ArcGIS Pro docs because CE Express is a separate browser-based product.

---

## Part 1 — CE Pro Documentation (ArcGIS Pro Screenshots)

These screenshots are from official ArcGIS Pro docs and match CE Pro docs directly because CE Pro is an ArcGIS Pro extension.

### Screenshot 1 — ArcGIS Pro Sign-In Window

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/sign-in-window-F405D.png` |
| **Type** | Screenshot |
| **Alt text** | ArcGIS Pro sign-in prompt |
| **Goes in** | `docs/ce-pro/training/00-installation.md` |
| **Note** | Insert after the "Activation" heading. Users must open ArcGIS Pro and sign in to activate CE Desktop license. |

---

### Screenshot 2 — ArcGIS Pro Sign-In Menu

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/sign-in-menu-F8B91.png` |
| **Type** | Screenshot |
| **Alt text** | Sign-in menu in an open ArcGIS Pro project |
| **Goes in** | `docs/ce-pro/training/00-installation.md` |
| **Note** | Insert below Screenshot 1. Shows the sign-in menu in the top bar of an open project. |

---

### Screenshot 3 — ArcGIS Pro Settings / Licensing Page

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/settings-page-8C3ED.png` |
| **Type** | Screenshot |
| **Alt text** | ArcGIS Pro settings page showing licensing options |
| **Goes in** | `docs/ce-pro/training/00-installation.md` |
| **Note** | Insert at the Licensing section. Users go to Project → Settings → Licensing to activate CE Desktop extension. |

---

### Screenshot 4 — ArcGIS Pro Start Page (Home Tab)

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/start-page-home-DC4BD.png` |
| **Type** | Screenshot |
| **Alt text** | The Home tab of the ArcGIS Pro start page |
| **Goes in** | `docs/ce-pro/training/04-workspace.md` |
| **Note** | Insert at the start of workspace creation steps. Shows where to click New Project. |

---

### Screenshot 5 — ArcGIS Pro Project View

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/arcgis-pro-project-3DC45.png` |
| **Type** | Screenshot |
| **Alt text** | ArcGIS Pro project with map view, Contents pane, and Catalog pane |
| **Goes in** | `docs/ce-pro/training/02-architecture.md` |
| **Note** | Insert at the top as an overview of the ArcGIS Pro interface. Shows map view, Contents pane and Catalog pane — the core layout when using CE Pro. |

---

### Screenshot 6 — ArcGIS Pro Ribbon (Core + Contextual Tabs)

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/ribbon_context_tab_diagram-D53F0.png` |
| **Type** | Screenshot / Diagram |
| **Alt text** | ArcGIS Pro ribbon showing core tabs and contextual CE tabs |
| **Goes in** | `docs/ce-pro/training/02-architecture.md` |
| **Note** | Insert after Screenshot 5. CE Pro tools appear as contextual tabs in the ribbon (Feature Layer, Labeling, Data tabs). |

---

### Screenshot 7 — Active Map View

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/arcgis-pro-view-AFCF6.png` |
| **Type** | Screenshot |
| **Alt text** | Active map view in ArcGIS Pro |
| **Goes in** | `docs/ce-pro/training/01-data-types.md` |
| **Note** | Insert near the top. Shows the map canvas where CE Pro data (sites, cells, predictions) is displayed. |

---

### Screenshot 8 — Contents Pane and Catalog Pane

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/contents-pane-catalog-pane-EDB2F.png` |
| **Type** | Screenshot |
| **Alt text** | Contents pane and Catalog pane in ArcGIS Pro |
| **Goes in** | `docs/ce-pro/training/01-data-types.md` |
| **Note** | Insert after Screenshot 7. CE Pro geodatabase and layers are managed here. |

---

### Screenshot 9 — Symbology Pane

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/pane-options-65B60.png` |
| **Type** | Screenshot |
| **Alt text** | Symbology pane with labelled controls |
| **Goes in** | `docs/ce-pro/training/06-objects.md` |
| **Note** | Insert in the section about styling network objects (sites/cells) on the map. |

---

### Screenshot 10 — Customised ArcGIS Pro UI Layout

| Field | Value |
|-------|-------|
| **URL** | `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/customize-ui-E4D73.png` |
| **Type** | Screenshot |
| **Alt text** | ArcGIS Pro interface with docked, stacked, and floating panes |
| **Goes in** | `docs/ce-pro/rcp-user-guide.md` |
| **Note** | Insert in a layout/tips section. Shows how to arrange panes for an efficient CE Pro workspace. |

---

## Part 2 — CE Express Documentation (Calcite Icons + Screenshots Needed)

CE Express is a **web browser application** — ArcGIS Pro screenshots do not apply here. Below are Esri Calcite icons (functional/concept icons) plus notes on where real CE Express screenshots are needed.

**Calcite icon URL pattern:** `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/{name}-32.svg`

---

### Icons for CE Express Docs

| # | Icon Name | URL | Alt Text | Goes In | Note |
|---|-----------|-----|----------|---------|------|
| 1 | `user` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/user-32.svg` | User / login icon | `docs/ce-express/login.md` | Use as the icon for the Login section heading or login button reference. |
| 2 | `map` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/map-32.svg` | Map icon | `docs/ce-express/overview.md` | Use next to "Map View" section heading. |
| 3 | `layers` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/layers-32.svg` | Layers icon | `docs/ce-express/workspace.md` | Use next to Workspace / geodata layers section. |
| 4 | `gear` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/gear-32.svg` | Settings icon | `docs/ce-express/user-guide/admin-guide-v7.2.md` | Use next to Administration / Settings headings. |
| 5 | `magnifying-glass` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/magnifying-glass-32.svg` | Search icon | `docs/ce-express/overview.md` | Use next to Search functionality reference. |
| 6 | `upload` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/upload-32.svg` | Import / upload icon | `docs/ce-express/training/05-import-data.md` | Use next to "Import Data" heading. |
| 7 | `download` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/download-32.svg` | Export / download icon | `docs/ce-express/training/05-import-data.md` | Use next to export/download data steps. |
| 8 | `graph-line` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/graph-line-32.svg` | Line graph / profile icon | `docs/ce-express/profile-tool.md` | Use next to "Line of Sight / Profile" heading. |
| 9 | `globe` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/globe-32.svg` | Globe / geodata icon | `docs/ce-express/geodata.md` | Use next to Geodata section heading. |
| 10 | `pin` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/pin-32.svg` | Location pin icon | `docs/ce-express/network-objects.md` | Use next to "Network Objects / Sites" heading. |
| 11 | `signal-tower` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/signal-tower-32.svg` | Cell tower icon | `docs/ce-express/network-objects.md` | Use next to "Cells / Antennas" heading. |
| 12 | `analysis` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/analysis-32.svg` | Analysis icon | `docs/ce-express/rf-prediction.md` | Use next to "RF Prediction" heading. |
| 13 | `raster` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/raster-32.svg` | Raster layer icon | `docs/ce-express/geodata.md` | Use next to DEM / raster geodata section. |
| 14 | `measure` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/measure-32.svg` | Measure / calculation icon | `docs/ce-express/training/04-rf-prediction.md` | Use next to prediction calculation steps. |
| 15 | `filter` | `https://raw.githubusercontent.com/Esri/calcite-ui-icons/master/icons/32/filter-32.svg` | Filter icon | `docs/ce-express/training/06-prediction-models.md` | Use next to model filter / selection steps. |

---

### CE Express Screenshots — Action Required

The following docs need real screenshots taken from the live CE Express web application. These **cannot** be replaced with ArcGIS Pro images.

| Doc File | Screenshot Needed | Where to Take It |
|----------|------------------|-----------------|
| `docs/ce-express/login.md` | CE Express login page | Open CE Express in browser → screenshot the login screen |
| `docs/ce-express/overview.md` | CE Express main map view | Log in → screenshot the full map interface |
| `docs/ce-express/workspace.md` | Workspace creation dialog | Map view → Workspaces tool → New Workspace dialog |
| `docs/ce-express/network-objects.md` | Sites and cells on map | Add a site and cell → screenshot the map with objects visible |
| `docs/ce-express/rf-prediction.md` | RF prediction panel + result raster | Run an RF prediction → screenshot panel and result on map |
| `docs/ce-express/profile-tool.md` | Profile / LOS tool panel | Draw a profile → screenshot the terrain cross-section result |
| `docs/ce-express/antenna-patterns.md` | Antenna pattern assignment dialog | Open a cell → assign antenna → screenshot the dialog |
| `docs/ce-express/street-view.md` | Street View panel inside CE Express | Open Street View tool → screenshot |
| `docs/ce-express/training/01-creating-workspace.md` | New workspace form | Workspaces → New → screenshot the form filled in |
| `docs/ce-express/training/09-preparing-geodata.md` | Geodata upload/configuration screen | Geodata settings → screenshot |

> **Who takes these:** Ask your senior developer or Elchin if CE Express is running on a server you can access, or if existing screenshots exist somewhere.

---

## Part 3 — ArcGIS Pro Icons (for CE Pro docs inline use)

Small 16px icons from ArcGIS Pro docs. Use these **inline** next to button/tab names in CE Pro documentation text.

| # | URL | Alt Text | Goes In | Note |
|---|-----|----------|---------|------|
| 1 | `https://doc.esri.com/en/arcgis-pro/latest/icons/HomeDefaultMonochrome16.png` | Home tab icon | `docs/ce-pro/training/04-workspace.md` | Inline next to "Home" tab reference |
| 2 | `https://doc.esri.com/en/arcgis-pro/latest/icons/GearDefaultMonochrome16.png` | Settings icon | `docs/ce-pro/training/00-installation.md` | Inline next to Settings tab in licensing steps |
| 3 | `https://doc.esri.com/en/arcgis-pro/latest/icons/BookDefaultMonochrome16.png` | Learning Resources icon | `docs/ce-pro/training/00-installation.md` | Inline next to Learning Resources tab |
| 4 | `https://doc.esri.com/en/arcgis-pro/latest/icons/FolderOpenState16.png` | Open folder icon | `docs/ce-pro/training/04-workspace.md` | Inline next to "Open another project" |
| 5 | `https://doc.esri.com/en/arcgis-pro/latest/icons/Find16.png` | Search / Find icon | `docs/ce-pro/training/02-architecture.md` | Inline next to command search reference |
| 6 | `https://doc.esri.com/en/arcgis-pro/latest/icons/ArcGISLearnColor16.png` | ArcGIS Learn icon | `docs/ce-pro/training/00-installation.md` | Inline next to Help → Learning Resources button |
| 7 | `https://doc.esri.com/en/arcgis-pro/latest/icons/List16.png` | List view icon | `docs/ce-pro/training/04-workspace.md` | Inline next to List view option on start page |
| 8 | `https://doc.esri.com/en/arcgis-pro/latest/icons/Grid16.png` | Grid / Tiles icon | `docs/ce-pro/training/04-workspace.md` | Inline next to Tiles view option |
| 9 | `https://doc.esri.com/en/arcgis-pro/latest/icons/Esri_BackButtonSmall.png` | Back button | `docs/ce-pro/training/02-architecture.md` | Inline when describing multi-page pane navigation |
| 10 | `https://doc.esri.com/en/arcgis-pro/latest/icons/auto-hide-button12.png` | Auto-hide icon | `docs/ce-pro/training/02-architecture.md` | Inline when describing how to auto-hide panes |

---

## Summary

| Category | Count | Status |
|----------|-------|--------|
| CE Pro screenshots (ArcGIS Pro) | 10 | ✅ Ready — URLs verified from official Esri docs |
| CE Pro inline icons (ArcGIS Pro) | 10 | ✅ Ready — URLs verified from official Esri docs |
| CE Express icons (Calcite SVG) | 15 | ✅ Ready — Esri open-source icon library |
| CE Express screenshots | 10 | ⚠️ Needed — must be taken from live CE Express app |

---

*Sources: [ArcGIS Pro docs](https://doc.esri.com/en/arcgis-pro/latest/get-started/get-started.html) · [Esri Calcite UI Icons](https://github.com/Esri/calcite-ui-icons) (Apache 2.0 license)*

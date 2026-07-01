# Visual Assets Catalog

This file lists all visual assets (screenshots and icons) to be integrated into the CE documentation.
Each entry includes the asset URL, type, and a note specifying **which documentation file** and **which section** the asset belongs in.

**Source:** All assets are sourced from official ArcGIS / Esri documentation.
**Integration:** Elchin will store these URLs in the PostgreSQL database and wire them into the portal.

---

## Screenshots

### 1. ArcGIS Pro Sign-In Window

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/sign-in-window-F405D.png`
- **Type:** Screenshot
- **Alt text:** ArcGIS Pro sign-in prompt
- **Goes in:** `docs/ce-pro/training/00-installation.md`
- **Note:** Insert after the "Activation" heading, where users are instructed to open ArcGIS Pro and sign in for the first time. Shows the sign-in dialog box.

---

### 2. ArcGIS Pro Sign-In Menu

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/sign-in-menu-F8B91.png`
- **Type:** Screenshot
- **Alt text:** Sign-in menu as it appears in an open project
- **Goes in:** `docs/ce-pro/training/00-installation.md`
- **Note:** Insert below screenshot #1, to show the sign-in menu in the top bar after signing in. Helps users identify where to switch accounts.

---

### 3. ArcGIS Pro Start Page — Home Tab

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/start-page-home-DC4BD.png`
- **Type:** Screenshot
- **Alt text:** The Home tab of the ArcGIS Pro start page
- **Goes in:** `docs/ce-pro/training/04-workspace.md`
- **Note:** Insert at the beginning of the "Creating a Workspace" steps, where the user opens ArcGIS Pro and sees the start page. Shows the New Project options.

---

### 4. ArcGIS Pro Start Page — Learning Resources Tab

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/start-page-learn-tab-B3D72.png`
- **Type:** Screenshot
- **Alt text:** The Learning Resources tab of the ArcGIS Pro start page
- **Goes in:** `docs/ce-pro/training/00-installation.md`
- **Note:** Insert in a "Getting Help" or "Additional Resources" note at the end of the installation doc. Shows users where to find ArcGIS Pro tutorials.

---

### 5. ArcGIS Pro Settings Page

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/settings-page-8C3ED.png`
- **Type:** Screenshot
- **Alt text:** ArcGIS Pro settings and licensing page
- **Goes in:** `docs/ce-pro/training/00-installation.md`
- **Note:** Insert at the Licensing section. Users must go to Project → Settings → Licensing to activate the CE Desktop extension. This screenshot shows exactly where that is.

---

### 6. ArcGIS Pro Project View

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/arcgis-pro-project-3DC45.png`
- **Type:** Screenshot
- **Alt text:** An ArcGIS Pro project with map view, Contents pane, and Catalog pane open
- **Goes in:** `docs/ce-pro/training/02-architecture.md`
- **Note:** Insert at the top of this doc as an overview of the ArcGIS Pro interface. Shows the relationship between map view, Contents pane, and Catalog pane — core to understanding CE Pro architecture.

---

### 7. ArcGIS Pro Ribbon — Core and Contextual Tabs

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/ribbon_context_tab_diagram-D53F0.png`
- **Type:** Screenshot / Diagram
- **Alt text:** ArcGIS Pro ribbon showing core tabs and contextual tabs
- **Goes in:** `docs/ce-pro/training/02-architecture.md`
- **Note:** Insert after screenshot #6, in the section that explains how CE Pro toolbar tabs appear in the ribbon. Contextual tabs (like Feature Layer, Labeling) are exactly how CE Pro tools appear in ArcGIS Pro.

---

### 8. ArcGIS Pro Active Map View

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/arcgis-pro-view-AFCF6.png`
- **Type:** Screenshot
- **Alt text:** An active map view in ArcGIS Pro with multiple open views
- **Goes in:** `docs/ce-pro/training/01-data-types.md`
- **Note:** Insert near the top. When explaining CE Pro data types, this shows the map canvas where all spatial data (sites, cells, predictions) is displayed.

---

### 9. Contents Pane and Catalog Pane

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/contents-pane-catalog-pane-EDB2F.png`
- **Type:** Screenshot
- **Alt text:** The Contents pane and Catalog pane in ArcGIS Pro
- **Goes in:** `docs/ce-pro/training/01-data-types.md`
- **Note:** Insert after the map view screenshot. CE Pro data (geodatabase, layers) is accessed via the Catalog pane, and all map layers appear in the Contents pane. Essential for understanding how CE data is organised.

---

### 10. Symbology Pane Controls

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/pane-options-65B60.png`
- **Type:** Screenshot
- **Alt text:** Symbology pane with labelled controls (tabs, expanders, menu button)
- **Goes in:** `docs/ce-pro/training/06-objects.md`
- **Note:** Insert in the section about viewing or styling network objects (sites/cells). The Symbology pane is used to change how CE network objects are displayed on the map.

---

### 11. Pane Overflow Menu

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/pane-overflow-menu-226FD.png`
- **Type:** Screenshot
- **Alt text:** Overflow menu for stacked panes in ArcGIS Pro
- **Goes in:** `docs/ce-pro/training/02-architecture.md`
- **Note:** Insert in the interface overview section. Explains how to navigate between multiple open panes (e.g. Contents, Catalog, CE Pro tool panes) when they are stacked.

---

### 12. ArcGIS Pro — Customised User Interface

- **URL:** `https://doc.esri.com/en/arcgis-pro/latest/get-started/images/customize-ui-E4D73.png`
- **Type:** Screenshot
- **Alt text:** ArcGIS Pro interface with docked and floating panes and views
- **Goes in:** `docs/ce-pro/user-guides/rcp-user-guide.md` *(or any CE Pro user guide that refers to screen layout)*
- **Note:** Insert in a tips section about arranging the workspace. Shows how users can dock, float, or stack panes to get the best layout when using CE Pro tools alongside standard ArcGIS panes.

---

## Icons

All icons below are 16×16 px PNG files from the official ArcGIS Pro icon set.

| # | Icon URL | Alt Text | Goes In | Note |
|---|----------|----------|---------|------|
| 1 | `https://doc.esri.com/en/arcgis-pro/latest/icons/HomeDefaultMonochrome16.png` | Home tab icon | `docs/ce-pro/training/04-workspace.md` | Use inline next to the word "Home" when describing the Home tab on the start page. |
| 2 | `https://doc.esri.com/en/arcgis-pro/latest/icons/BookDefaultMonochrome16.png` | Learning Resources tab icon | `docs/ce-pro/training/00-installation.md` | Use inline next to "Learning Resources" tab reference. |
| 3 | `https://doc.esri.com/en/arcgis-pro/latest/icons/GearDefaultMonochrome16.png` | Settings / Gear icon | `docs/ce-pro/training/00-installation.md` | Use inline next to "Settings" tab in the licensing activation steps. |
| 4 | `https://doc.esri.com/en/arcgis-pro/latest/icons/FolderOpenState16.png` | Open Folder icon | `docs/ce-pro/training/04-workspace.md` | Use inline when referring to "Open another project" or browsing for geodata folder. |
| 5 | `https://doc.esri.com/en/arcgis-pro/latest/icons/List16.png` | List view icon | `docs/ce-pro/training/04-workspace.md` | Use inline next to "List" view option on the start page. |
| 6 | `https://doc.esri.com/en/arcgis-pro/latest/icons/Grid16.png` | Tiles / Grid view icon | `docs/ce-pro/training/04-workspace.md` | Use inline next to "Tiles" view option on the start page. |
| 7 | `https://doc.esri.com/en/arcgis-pro/latest/icons/ArcGISLearnColor16.png` | ArcGIS Learn icon | `docs/ce-pro/training/00-installation.md` | Use inline when referencing the Help tab → Learning Resources button. |
| 8 | `https://doc.esri.com/en/arcgis-pro/latest/icons/Find16.png` | Find / Search icon | `docs/ce-pro/training/02-architecture.md` | Use inline next to "Locate" or command search references in the ribbon overview. |
| 9 | `https://doc.esri.com/en/arcgis-pro/latest/icons/Esri_BackButtonSmall.png` | Back button icon | `docs/ce-pro/training/02-architecture.md` | Use inline when describing multi-page pane navigation. |
| 10 | `https://doc.esri.com/en/arcgis-pro/latest/icons/GenericList12.png` | Pane menu button icon | `docs/ce-pro/training/02-architecture.md` | Use inline next to the "Menu button" reference in the pane controls section. |
| 11 | `https://doc.esri.com/en/arcgis-pro/latest/icons/auto-hide-button12.png` | Auto-hide pane icon | `docs/ce-pro/training/02-architecture.md` | Use inline when describing how to auto-hide the Contents or Catalog pane to save screen space. |
| 12 | `https://doc.esri.com/en/arcgis-pro/latest/icons/BookMonochrome16.png` | Book (monochrome) icon | `docs/ce-pro/training/00-installation.md` | Use inline as an alternative to BookDefaultMonochrome16 where a monochrome style is preferred. |

---

## Summary Table

| Asset | Type | Destination File |
|-------|------|-----------------|
| Sign-in window | Screenshot | `ce-pro/training/00-installation.md` |
| Sign-in menu | Screenshot | `ce-pro/training/00-installation.md` |
| Start page Home tab | Screenshot | `ce-pro/training/04-workspace.md` |
| Start page Learning Resources tab | Screenshot | `ce-pro/training/00-installation.md` |
| Settings page | Screenshot | `ce-pro/training/00-installation.md` |
| ArcGIS Pro project view | Screenshot | `ce-pro/training/02-architecture.md` |
| Ribbon contextual tabs diagram | Screenshot | `ce-pro/training/02-architecture.md` |
| Active map view | Screenshot | `ce-pro/training/01-data-types.md` |
| Contents and Catalog panes | Screenshot | `ce-pro/training/01-data-types.md` |
| Symbology pane controls | Screenshot | `ce-pro/training/06-objects.md` |
| Pane overflow menu | Screenshot | `ce-pro/training/02-architecture.md` |
| Customised UI layout | Screenshot | `ce-pro/rcp-user-guide.md` |
| Home icon | Icon | `ce-pro/training/04-workspace.md` |
| Book / Learning icon | Icon | `ce-pro/training/00-installation.md` |
| Settings / Gear icon | Icon | `ce-pro/training/00-installation.md` |
| Open Folder icon | Icon | `ce-pro/training/04-workspace.md` |
| List view icon | Icon | `ce-pro/training/04-workspace.md` |
| Tiles / Grid icon | Icon | `ce-pro/training/04-workspace.md` |
| ArcGIS Learn icon | Icon | `ce-pro/training/00-installation.md` |
| Find / Search icon | Icon | `ce-pro/training/02-architecture.md` |
| Back button icon | Icon | `ce-pro/training/02-architecture.md` |
| Pane menu button icon | Icon | `ce-pro/training/02-architecture.md` |
| Auto-hide icon | Icon | `ce-pro/training/02-architecture.md` |
| Book monochrome icon | Icon | `ce-pro/training/00-installation.md` |

---

*Sources: [ArcGIS Pro documentation](https://doc.esri.com/en/arcgis-pro/latest/get-started/get-started.html) · [ArcGIS Maps SDK for JavaScript](https://developers.arcgis.com/javascript/latest/)*

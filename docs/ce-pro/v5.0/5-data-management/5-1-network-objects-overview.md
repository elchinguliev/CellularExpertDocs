# Network Objects

Cellular Expert network objects represent the physical and logical elements of a radio network on the map. With the data management tools in the Data Management group, you can view and edit these objects.

> **Note:** Most data management tools work only in editing sessions on the currently active workspace.

## Object Types

| Object | Description |
|---|---|
| **Site** | Represents the geographical location of a radio station (tower). Identified by a unique Site ID and holds the geographical coordinates, ground altitude, and base height. |
| **Cell** | The primary network object used for coverage prediction calculations. Holds the carrier list, equipment information, height, and other common radio channel parameters. |
| **Sirens** | Represents a sound-emitting warning/alerting device and its geographical location. Holds the parameters required for siren sound-level prediction. |
| **Radar** | Represents the geographical location of a radiolocation system that uses radio waves to determine the distance, angle, and radial velocity of objects. |
| **CPE** | Customer Premises Equipment — represents the geographic location of a client/subscriber. |
| **Repeater** | Represents the geographical location of a signal repeater, used to extend wireless coverage by amplifying and retransmitting signals for microwave point-to-point network planning with Links. |
| **Satellite** | A GEO satellite template used by the SAT link-budget and visibility tools. |
| **Ground Station** | Represents a fixed, earth-based satellite terminal, including its antenna and link parameters. |
| **Link** | Represents a radio connection between a transmitter and a receiver, operating at a fixed frequency from the transmitter's carrier list. |
| **Mesh Node** | Represents a node used in mesh network calculations and serves as an endpoint for Link objects. |

## Object Availability by Module

Not every module exposes a dedicated **Add Object** workflow for every object type above. The table below reflects the object types each module can create directly:

| Module | Dedicated Add Object workflows |
|---|---|
| **SAT** | [Satellite](5-2-add-object/5-2-4-sat/5-2-4-1-add-satellite.md), [Ground Station](5-2-add-object/5-2-4-sat/5-2-4-2-add-ground-station.md) |
| **Sound** | [Cell](5-2-add-object/5-2-1-add-cell.md) |
| **EMF** | [Cell](5-2-add-object/5-2-1-add-cell.md) |
| **Indoor** | [Cell](5-2-add-object/5-2-1-add-cell.md) |
| **RCP** | [Cell](5-2-add-object/5-2-1-add-cell.md), [Site](5-2-add-object/5-2-5-rcp/5-2-5-1-add-site.md), [Radar](5-2-add-object/5-2-5-rcp/5-2-5-2-add-radar.md), [Sirens](5-2-add-object/5-2-5-rcp/5-2-5-3-add-sirens.md), [CPE](5-2-add-object/5-2-5-rcp/5-2-5-4-add-cpe.md), [Repeater](5-2-add-object/5-2-5-rcp/5-2-5-5-add-repeater.md) |
| **RLP** | [Site](5-2-add-object/5-2-6-rlp/5-2-6-1-add-site.md), [Link](5-2-add-object/5-2-6-rlp/5-2-6-2-add-link.md), [Mesh Node](5-2-add-object/5-2-6-rlp/5-2-6-3-add-mesh-node.md) |

> **Note:** RCP's Site object is used only in 4G/5G carrier-aggregation calculations (Total Downlink Throughput). RLP's Site object shares the same object name but has a materially different field set — see its own [Add Site](5-2-add-object/5-2-6-rlp/5-2-6-1-add-site.md) page.

New network objects can be created in several ways:

- Imported using the CE for ArcGIS Pro functionality — see [Import Objects](5-9-import-objects.md).
- Created with Cellular Expert tools from zero, defining all parameters in the process — see [Add Object](5-2-add-object/5-2-1-add-cell.md).
- Created from templates — see [Feature Set Templates](5-2-add-object/5-2-2-feature-set-templates.md) and [Template Manager](5-8-template-manager.md).

The Add Object dockpane exposes three tabs with different functionality for adding objects: **Network Objects**, **Feature Set Templates**, and **Batch Creation**.

Once created, objects can be repositioned or duplicated with the [Object Editor](5-3-object-editor.md) (or the [RLP Object Editor](5-4-rlp-object-editor.md) for RLP).

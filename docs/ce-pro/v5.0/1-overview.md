# CE Pro Overview

Cellular Expert Desktop for ArcGIS Pro (CE Pro) is a family of licensed modules — **SAT**, **Sound**, **EMF**, **Indoor**, **RCP**, and **RLP** — built on the same ArcGIS Pro extension. This guide documents the functionality shared across all six modules, with module-specific tools and workflows called out separately where they apply.

## Software Purpose and Functionality

Cellular Expert Desktop for ArcGIS Pro (CE Pro) is a professional radio coverage planning software tool designed on top of the Esri ArcGIS Pro environment. CE Pro is a highly versatile and functional tool, covering the network design functionality needs of most professional radio communication planners and developers. It supports network planning and optimization for the entire range of wireless technologies in frequencies from 10 kHz to 350 GHz.

The key features and benefits of utilizing Cellular Expert software are as follows:

1. CE Pro is a purpose-built extension of ESRI software, a world-renowned standard in GIS environments. This means that along with wireless network planning and optimization, it gives users various value-added GIS/mapping functionalities to manage, visualize feature classes or rasters, create reports and graphs, or automate workflows.
2. CE Pro is made of several processing engines and functional modules and therefore may be easily configured for various business functions: network planning, network engineering, technology information support to sales and marketing, network assets management, and network operational maintenance and supervision.
3. CE Pro is maintained and constantly developed by a dedicated agile team of software developers and radio planners, allowing attentive responsiveness to customer needs and developing custom-tailored solutions.

CE Pro performs mobile network coverage analysis based on:

1. Site and cell level details of radio equipment complement, specifications, cell and component carrier configuration.
2. Subscriber characteristics — geographic distribution density, generated traffic — used to estimate network/cell loading.
3. DTM, buildings, and clutter-based deterministic point-to-area radio wave propagation modeling.

CE Pro allows the user to input and use a broad variety of GIS and network data to support the simulations, as the overall quality of coverage calculations is dependent on the completeness and detail of technical network data and the resolution and quality of the GIS data. CE Pro can efficiently simulate wide area network coverage using GIS data with a resolution down to sub-meter.

Calculated results of coverage predictions can be presented as coverage raster maps. CE Pro is capable of modeling various wireless technologies: cellular (2G/3G/4G/5G), PMR/PAMR (TETRA, APCO, others), FWA/BWA, IoT (LoRa/SigFox, others), as well as fixed microwave links. It may therefore be used as a radio planning tool in various industries: Mobile Operators, Integrated Telecom Companies, Wireless Internet Service Providers, Regulatory Authorities, Utilities, Broadband Infrastructure Providers, Defense organizations, as well as any other users of radiocommunication systems.

The key functionalities of the tool are summarized below.

**Data Management**

The tool allows the importation, storage, and management of detailed technical data on network nodes, such as sites, cells, RF transmitters, and antennas.

**Signal Strength Prediction**

The tool contains several in-built path loss prediction models that allow the user to easily start simulations based on the evaluation of the most essential pathloss contributing factors. The following two models constitute the starting set:

- **Free space** — typically used for modeling short-range mobile communications, fixed links, or other radiocommunications applications with prevalent Line-of-Sight conditions on propagation paths.
- **UniMacro** — a proprietary universal model for wide area mobile communication systems that flexibly accounts for a variety of propagation paths as determined for each specific reception point based on terrain and clutter data vs. configuration of the modeled system.

Further details on path loss models and their configuration options are provided in [Prediction Model Manager](5-data-management/5-7-prediction-model-manager.md).

**Model Tuning**

The tool provides an automated method for fine-tuning propagation model parameters to fit the specific scenario and type of area of network deployment based on analyzing real field strength measurement results.

**Radio Coverage Calculation for Different Mobile Technologies**

Radio coverage calculation is assisted in the tool by the possibility to use pre-loaded cell configuration templates that are tailored to typical technical parameters of base stations in different Radio Access Technologies. Accordingly, the model settings and outputs are adjusted to suit the scenario pertinent to that technology:

- **2G** — radio coverage is calculated in dBm as the receive power level of a narrow-band (200 kHz) signal.
- **3G** — radio coverage is calculated in dBm as the receive power level of a single broadband (3.85 MHz) carrier.
- **4G/5G** — radio coverage is calculated in dBm as the equivalent RSRP of a single sub-carrier component in the complex OFDM broadband signal.
- **Wi-Fi** — wireless communication technology based on the IEEE 802.11 standards, used for setting up local area networks (WLANs) and providing internet access without requiring cable connections.

**Profile Analysis**
The tool provides powerful GIS analytical features to analyze the terrain and clutter on the fixed link path, allowing the estimation of Fresnel zone clearance condition, Power Budget, Path loss, and Angles between Tx and Rx.

## License Types

Only a Single Use Cellular Expert license is available. The license type is annual and dedicated to one workstation connected with ArcGIS Online, which is used for ArcGIS Pro.

### Single-User Environment

For the Single-User configuration of Cellular Expert, all information about radio network objects is stored in a personal geodatabase (GDB format) or locally on the disk (calculation results, raster data in GeoTIFF format, etc.).

Geographical data can be stored:

- Locally on a disk.

An ArcGIS Pro license and an active ArcGIS Named User or ArcGIS Pro Standalone license are required to operate in the Single-User environment.

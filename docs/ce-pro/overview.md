# CE Desktop Pro — Overview / Getting Started

> **Note:** Applies to: RCP, RLP, EMF, Indoor, and Sound. If a module has a small difference, see the module-specific tools page.

## 1. Software Purpose and Functionality

CE Pro runs as an extension inside ArcGIS Pro. For an efficient CE Pro workspace, arrange your panes so the map, Contents, and CE Pro tools are all visible at once:

Cellular Expert Desktop for ArcGIS Pro (CE Pro) is a professional radio coverage planning software tool
designed on top of the Esri ArcGIS Pro environment. The CE Pro is a highly versatile and functional tool,
covering the network design functionality needs of most professional radio communication planners and
developers. It could support network planning and optimization for the entire range of wireless technologies
in frequencies from 10 kHz to 350 GHz.
The key features and benefits of utilizing Cellular Expert software are as follows:

1. CE Pro is a purpose-built extension of ESRI software, a world-renowned standard in GIS
environments. This means that along with wireless network planning and optimization, it gives
users various value-added GIS/mapping functionalities to manage, visualize feature classes or
roasters, create reports, and graphs, or automate workflows,

2. CE Pro is made of several processing engines and functional modules and therefore may be
easily configured for various business functions: network planning, network engineering,
technology information support to sales and marketing, network assets management, and
network operational maintenance and supervision,

3. CE Pro is maintained and constantly developed by a dedicated agile team of software
developers and radio planners, allowing attentive responsiveness to customer needs and
developing custom-tailored solutions.
CE Pro performs mobile network coverage analysis based on:

1. Site and cell level details of radio equipment complement, specifications, cell and component
carriers configuration,

2. Subscriber characteristics – geographic distribution density, generated traffic to estimate
network/cell loading,

3. DTM, buildings, and clutter-based deterministic point-to-area radio wave propagation
modeling.
CE Pro allows the user to input and use a broad variety of GIS and network data to support the simulations,
as the overall quality of coverage calculations is dependent on the completeness and detail of technical
network data and the resolution and quality of the GIS data. CE Pro can efficiently simulate wide area
network coverage using the GIS data with a resolution of down to sub-meter.
Calculated results of coverage predictions could be presented as coverage raster maps.
CE Pro is capable of modeling various wireless technologies: cellular (2G/3G/4G/5G), PMR/PAMR
(TETRA, APCO, others), FWA/BWA, IoT (LoRa/SigFox, others), as well as fixed microwave links.
Therefore, it may be used as a radio planning tool in various industries: Mobile Operators, Integrated
Telecom Companies, Wireless Internet Service providers, Regulatory authorities, Utilities, Broadband
Infrastructure providers, Defense organizations, as well as any other users of radiocommunication systems.
In the following, we summarize the key functionalities of the tool.
Data Management
The tool allows the importation, storage, and management of detailed technical data on network nodes,
such as sites, cells, RF transmitters, and antennas.
Signal Strength Prediction
The tool contains several in-built path loss prediction models that allow the user to easily start simulations
based on the evaluation of the most essential pathloss contributing factors. The following two models
constitute the starting set:
• Free space – typically used for modeling short-range mobile communications, fixed links, or other
radiocommunications applications with prevalent Line-of-Sight conditions on propagation paths,

• UniMacro – a proprietary universal model for wide area mobile communication systems that flexibly
accounts for a variety of propagation paths as determined for each specific reception point based
on terrain and clutter data vs. configuration of the modeled system.
Further details on path loss models and their configuration options are provided in the relevant section of
this manual.
Model Tuning
The tool provides an automated method for fine-tuning propagation model parameters to fit the specific
scenario and type of area of network deployment based on analyzing real field strength measurement
results.
Radio Coverage Calculation for Different Mobile Technologies
Radio coverage calculation is assisted in the tool by the possibility to use pre-loaded cell configuration
templates that are tailored to typical technical parameters of base stations in different Radio Access
Technologies. Accordingly, the model settings and outputs will be adjusted to suit the scenario pertinent to
that technology, i.e.:
• 2G – radio coverage is calculated in dBm as receive power level of narrow-band (200 kHz) signal,
• 3G – radio coverage is calculated in dBm as the receive power level of a single broadband (3.85
MHz) carrier,
• 4G/5G – radio coverage is calculated in dBm as the equivalent RSRP of a single sub-carrier
component in the complex OFDM broadband signal.
• Wi-Fi - wireless communication technology based on the IEEE 802.11 standards, used for setting
up local area networks (WLANs) and providing internet access in various settings without requiring
cable connections.
Profile Analysis
The tool provides powerful GIS analytical features to analyze the terrain and clutter on the fixed link path,
such as allowing to estimate of the Fresnel zone clearance condition, Power Budget, Path loss and Angles
between Tx and Rx.

## 2. System requirements
This chapter will guide you through the minimal hardware and software requirements.
Note: requirements can vary significantly, depending on the acceptable calculation time and task
complexity.

### 2.1 Minimal Requirements for Hardware
Processor (CPU):
• Minimum: 8 cores, hyperthreaded
• Recommended: 16 cores
(Optional) Requirements for GPU-accelerated calculations
• GPU – any NVIDIA GPU with CUDA capabilities (https://developer.nvidia.com/cuda-gpus)
• Driver version: 456.38 or later
• CUDA Toolkit 11.0 or later
Memory/RAM:
• Minimum: 16 GB
• Recommended: 32 GB
Storage:
• Minimum: 500 GB of free space
• Recommended: 2TB or more of free space on a solid-state drive (SSD)

### 2.2 Minimal Requirements for Software
Cellular Expert runs on Microsoft Windows 10 or higher operating system.
It requires:
• Microsoft .NET 8.0:
Download .NET 8.0 Desktop Runtime (v8.0.0) - Windows x64 Installer
• Microsoft Visual C++ Redistributable packages 2015-2022:
https://aka.ms/vs/17/release/vc_redist.x64.exe
• .NET support for ArcGIS libraries
• ArcGIS Pro from version 3.3.x

## 3. License types
Only a Single Use Cellular Expert license is available. The license type is annual and dedicated to one
workstation connected with ArcGIS Online, which is used for ArcGIS Pro.

### 3.1 Single-User Environment
For the Single-User configuration of Cellular Expert, all information about radio network objects is stored in
a personal geodatabase (GDB format) or locally on the disc (calculation results, raster data in GeoTIFF
format, etc.).
Geographical data can be stored:
• Locally on a disc
An ArcGIS Pro license and an active ArcGIS Named User or ArcGIS Pro Standalone are required to operate
in the Single-User environment.

## 4. Getting Started
Welcome to Cellular Expert.
This chapter will guide you through project creation and analysis. It includes the installation and preparation
of the Cellular Expert extension, as well as using it for the first time and creating a project.
Note: the tools are not explained in this chapter. They are referenced in other chapters of this guide.

### 4.1 Installation
• If applicable, uninstall the previous version of Cellular Expert for ArcGIS Pro
• Make sure that .NET 8.0 is installed
• Make sure that ArcGIS Pro 3.3.x is installed
• Run the ceProSetup.msi file to install the new version of Cellular Expert for ArcGIS Pro
• After successful installation, open Task Manager > Services, and run CE_Pro_Prediction_Service

### 4.2 Activation
This step is required for new users. If the Cellular Expert for ArcGIS Pro license has already been activated,
please skip this step.
You can activate the license in two ways:
First way:

1. Open ArcGIS Pro and select Settings

2. Navigate to Licensing → External Extensions

3. Find the Cellular Expert entry in the extensions table

4. Click the checkmark in the Enabled field. The License Activation dialog will appear

5. Copy the User Key and send it to support@cellular-expert.com. You will be provided with a
License Activation Key which must be entered into the same dialogue

6. Press Activate License and the license will be activated, enabling the acquired versions of the
add-on
Second way:

1. Create an empty ArcGIS Pro project

2. Navigate to Insert and select New Map. After the map insertion, the Cellular Expert tabs will be
enabled

3. Navigate to any of the Cellular Expert tabs and select License Information in the About section.

4. Copy the User Key and send it to support@cellular-expert.com. You will be provided with a
License Activation Key which must be entered into the same dialogue

5. Press Activate License and the license will be activated, enabling the acquired versions of the
add-on
If you want to check the expiration date of the license you can:

1. Open ArcGIS Pro and start/open a project with an active map

2. Navigate to the Cellular Expert tab

3. Select License Information in the About section

If you encounter any problems or want additional details about the license, please contact Cellular Expert
at support@cellular-expert.com. For more information, see the chapter Technical Support.

### 4.3 Tools
The Cellular Expert tools are in the Cellular Expert add-on. They appear automatically after installation of

![Image p11](../assets/images/ce-pro/rcp-guide/p011-img1.png)

![Image p11](../assets/images/ce-pro/rcp-guide/p011-img2.png)

![Image p11](../assets/images/ce-pro/rcp-guide/p011-img3.png)

![Image p11](../assets/images/ce-pro/rcp-guide/p011-img4.png)
CE for ArcGIS Pro and will be found in the menu ribbon.
There are 5 types of licenses and therefore 5 different tabs with various tool configurations:
• RCP
• RLP

• EMF
• Sound
• Indoor
This User Guide describes RCP tools.

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img1.png)

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img2.png)

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img3.png)

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img4.png)

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img5.png)

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img6.png)

![Image p12](../assets/images/ce-pro/rcp-guide/p012-img7.png)

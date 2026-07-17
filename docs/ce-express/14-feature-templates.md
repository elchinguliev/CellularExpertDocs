# Feature Templates

> **Version:** CE Express v7.3

Feature templates let you quickly fill out feature parameters from pre-saved data. Use them when creating features or when running calculations where a cell is missing required parameters.

---

Color – the color by which the clutter class is represented in different UI elements, for example – the profile
chart.
3.1.8 Feature templates
Feature templates serve the purpose of allowing the user to quickly fill out feature parameters from pre-
saved data. In the case of feature creation, you can fill out the parameters by selecting a feature template
in the add features tool. In the case of starting some calculations, you may pick a template from which
missing feature parameters will be filled during the calculation. The feature templates tool allows you to set
up these templates before using them.

After opening the tool, you get to choose which feature type you want to manage templates for.
After selecting the feature type, a list of existing feature templates is shown, click an existing feature
template to edit it, or click new feature template to create a new one.

Upon hovering the mouse over a feature template, options for it appear.
Mark as favorite
Delete Feature template
3.1.9 Prediction models
Click this button to open Prediction models tool.
The CE Path Loss Modelling aims to perform near-deterministic calculation of received signal levels at each
specific point (pixel) in the network’s target coverage area by applying selective path loss model depending
on the radio visibility condition between the transmitter antenna vis-à-vis a receiver antenna located at a
given point in coverage area. The radio visibility is evaluated based on the DTM, Obstacles and Clutter
path profile information. This verification of radio visibility will result in the receiver antenna point assigned
into one of three possible radio visibility conditions:
• Line-of-Sight (LOS) – occurs when there are neither terrain irregularities, obstacles or clutter
interposing the direct radio path between the transmitter and receiver antennas. The radio path is
understood to include the 1st Fresnel zone around the direct line and account for Spherical Earth
effect. The LOS condition is illustrated by the path profile depicted in Fig. 3(a).
• Obstructed LOS (OLOS) – occurs when the direct radio propagation line is interposed by clutter,
see illustration in Fig. 3(b).
• Non-LOS (NLOS) – occurs when the direct radio propagation line is interposed by terrain bulges
or obstacles, see illustration in Fig. 3(c).

a. Example of path profile with LOS condition (green line of direct radio link)
b. Example of path profile with OLOS condition (yellow segment of radio link path)
(c) Example of path profile with NLOS condition (red segment of radio link path)

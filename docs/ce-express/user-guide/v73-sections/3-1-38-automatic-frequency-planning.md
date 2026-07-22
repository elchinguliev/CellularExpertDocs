# 3.1.38 Automatic frequency planning

Click this button ![icon](../../../assets/images/ce-express/user-guide-v73/p220-img2.png) to open Automatic frequency planning tool.
The automatic frequency planning tool for each selected link suggests the best channel from the chosen
frequency plan and the selected channel list. It considers inter-link interference, evaluates signal-to-
interference ratio (SIR) across available carriers, and aims to maximize link performance while minimizing

![Image p220](../../../assets/images/ce-express/user-guide-v73/p220-img1.png)
co-channel interference. The tool accounts for duplex link pairing, node-layer priority, and site location
constraints (e.g., neighboring links and links sharing the same site).

Automatic frequency planning
Calculation name
Name of the calculation that will be displayed in Prediction history.
Link template
Template to be used for filling up missing parameters of the link.
Frequency plan
Frequency plan
Frequency plan that is applied to the links.
Recalculate already planned frequencies
Where applicable, the tool respects existing channel assignments. If frequency recalculation is explicitly

![Image p221](../../../assets/images/ce-express/user-guide-v73/p221-img1.png)
enabled, i.e., the Recalculate already planned frequencies option is checked, the frequencies are
reassigned for all links regardless of whether they have channel assignments.
The resulting plan includes the assigned frequency, polarization, best available modulation and SIR
score.

Assign channels
Assign suggested channel & polarization values to link objects.

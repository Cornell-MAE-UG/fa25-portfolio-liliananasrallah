---
layout: project
title: MAE 4272 Turbine Blade Design
description: Design Project
technologies: MATLAB, Fusion360, excel
image: /assets/images/bladetwist.jpeg
--- 

## Overview

For MAE 4272: Fluids and Heat Transfer Laboratory, we were asked to design a small scale wind turbine blade that would maximize power output while retaining structural stability. Because of the small scale, our turbine blades were designed to operate in low Reynolds number regimes. The design also had to adhere to several dimensional and operational constraints as listed below. 
- Blade length must be below 6 inches not including attachment piece.
- Blade must be able to integrate with hub attachment piece.
- Axial clearance must be less than 2 inches to avoid interferrence with nacelle.
- Turbine must remain under 3500 RPM during testing.
- Wind tunnel must be running below 15 Hz which corresponds to a wind speed of 9.8 m/s.
- Torque generated must stay below torque brake maximum of 3.5 Ncm.
- Maximum bending stress must remain below flexural stress of material of 44 MPa.

![photo of blade in wind tunnel]({{ "/assets/images/windtunnel.jpeg" | relative_url }}){: .inline-image-r style="width: 200px"}


## Design Process

The first step in our design process was selecting an airfoil cross-section. We researched several different airfoil types on airfoiltools.com, focusing on airfoils that performed well at low Reynolds numbers (Re = 100,000), and made a table listing key characteristics. We decided to use the SG6043 airfoil because it has high lift at the ideal angle of attack, it is not too thin so it will be structurally stable, and it does not have strange geometry that might provide problems during printing. Then, we decided on a blade length of 6 inches because longer blades generate more power. We designed our blade to operate best at a wind speed of 5 m/s because that was the most probable wind speed according to the provided Weibull distribution. We chose our operating RPM to be 1880, which corresponds to a tip speed ratio of 6 at the rated wind speed. Next, we used a set of equations for ideal rotor without wake rotation from the textbook *Wind Energy Explained* to find our chord and pitch distributions. We also experimented with using a linear chord distribution because the larger chord lengths provided more structural stability. We evaluated the power generation and factor of safety of these different iterations in a MATLAB script that implemented blade element momentum theory and modeled the blades as cantilevered beams. In the end, we decided to used an chord distribution that was averaged between the calculated and linear distributions because this resulted in a sufficiently large factor of safety while also optimizing power generation. A picture of the CAD model of our final blade design is shown below.

![photo of final blade]({{ "/assets/images/bladechord.jpeg" | relative_url }})
** Figure 1. ** CAD model of blade design. 


## Testing Summary

To test our blade design in the wind tunnel, we collected power curves at a range of wind speeds from 3-5.5 m/s. Once the wind tunnel was set to the desired wind speed and the turbine was spinning, we would gradually increase the applied torque from the torque brake until the turbine stalled. After adjusting the torque, we would wait 10-20 seconds before collecting data to allow steady state to be reached. Then, once we had our power curves, we used linear interpolation to find the power generated at our target RPM of 1880 for each wind speed. However, there was one wind speed (3 m/s) where our turbine never reached our target RPM even at free spin, as shown in Figure 2 below. Additionally, during testing we were running short on time, so some of our data appears a bit inconsistent because we might not have allowed enough time for the system to reach steady state. 

![photo of final blade]({{ "/assets/images/wind tunnel results.jpeg" | relative_url }})
** Figure 2. ** Experimental Power Curves. 


## My Contributions

- Researched different airfoils and compared key characteristics.
- Wrote MATLAB code to predict and compare the performance of different blade designs.
- Assisted with operating wind tunnel during testing and watching for stalling or safety concerns.
- Contributed to progress report, experimental procedure, presentation, and design report writing.


---
title: "Aiot"
date: 2023-08-10T22:57:47+05:30
author: "Nithish K Gnani"
draft: false
---
---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: March 2019 - February 2020  
💰 Funded by: Boeing  
👩‍🏫 Guided by: [Dr. TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/)  

---
# Summary
Modern aircraft are replete with IoT sensors, but storage limitations necessitate data reduction, risking the loss of critical information. Our solution lies in judiciously aggregating time-series data, optimizing storage during flight and enabling post-flight analysis.  
Central to our work is real-time aircraft cabin air quality monitoring. Employing the MATLAB-Simulink Aircraft Environmental Control System (ECS) model, we simulated cabin conditions. Our system integrates supervised machine learning with simulated time-series data, enabling meticulous air quality assessment and anomaly resolution. Vital parameters - CO2, temperature, pressure, and humidity - undergo real-time monitoring, using a customized Adaptive Decision Block for anomaly classification. Based on the criticality of the data, an adaptive storage mechanism is used to save on storage space and allow for accurate reconstruction. 

{{< figure src="/img/aiot/cabin-sim.png" >}}

## Modules in the project
{{< figure src="/img/aiot/aiot-modules.png" >}}

### Cabin simulation
Aircraft cabin ECS system using Simulink. Various parameters such as passenger count, flight duration, and passenger activity can be set using a GUI developed in MATLAB. The cabin is divided into 6 zones. A diffusion model was written to simulate the flow of particles across the cabin. 
{{< figure src="/img/aiot/aiot-gui.png" caption="AIOT GUI using MATLAB">}}

{{< figure src="/img/aiot/class2-anomaly.png" caption="Example - Class 2 anomaly in zone 2 for 50% occupancy">}}

### Anomaly and severity level prediction
{{< figure src="/img/aiot/anomaly-detection.png" caption="Anomaly & severity level prediction logic">}}

{{< figure src="/img/aiot/adaptive-decision-block.png" caption="Adaptive decision block">}}

{{< figure src="/img/aiot/anomaly-severity.png" caption="Example of anomaly & severity level prediction">}}

### Storage space savings using linear prediction

In this method, lines are interpolated on the time-series data. The points which are deviating from the line within an error threshold are dropped such that the values do not differ drastically from actual values. This enables faithful reconstruction of data when required.

{{< figure src="/img/aiot/adaptive_storage_logic.gif" caption="Adaptive storage">}}

### Cost function to determine error threshold
There is an inverse relationship between error threshold and storage space consumed. Larger errors allow us to consume less space but reduce reconstruction accuracy. An optimum error threshold needs to be chosen depending on available storage space and the severity of data.
This optimization is done using cost functions over windows (batches) of time series data
{{< figure src="/img/aiot/aiot-cost-function1.png" >}}

### Implementation in TICK stack
The time-series data we generate is fed into a temporary database of InfluxDB block in TICK stack. Our adaptive storage algorithm runs in the Kapacitor block and stored into the final database. Chronograf is used whenever reconstruction of data is required.
{{< figure src="/img/aiot/TICK-stack.png" >}}

## Results
##### Storage space savings obtained: 96.6%
{{< figure src="/img/aiot/aiot-result-percent.png" >}}
The data stored and the reconstruction from the sparsely stored data can be seen in the figures below.
{{< load-photoswipe >}}
{{< gallery dir="/img/aiot/aiot-results" />}}

### Future
The results and observations in this project inspired the work on data management in energy-constrained IoT sensor nodes that transmit data wirelessly.  
_Judicious data management for sustaining an energy harvesting sensor node, Concurrency and Computation: Practice and Experience. https://doi.org/10.1002/cpe.5997_

---
#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Sachin SM](https://www.linkedin.com/in/sachin-s-m-040288124), [Pratyush Shukla](https://www.linkedin.com/in/pratyush-shukla/%20%20)

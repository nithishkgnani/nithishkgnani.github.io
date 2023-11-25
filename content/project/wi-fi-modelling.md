---
title: "Wi Fi Modelling"
date: 2020-07-01
author: "Nithish K Gnani"
draft: false
---
---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: July 2020 - June 2021  
💰 Funded by: Boeing  
👩‍🏫 Guided by: [Prof. Neelesh Mehta](https://ece.iisc.ac.in/~nextgenwrl/Neelesh.html) and [Prof. Chandramani Singh](https://faculty.dese.iisc.ac.in/chandramani/)  

---

# Objective
1. Modeling and simulation of physical and MAC layers of IEEE WLANs to obtain the performance metrics for various scenarios of an aircraft moving in an airport.  
2. Standards considered: 802.11n & 802.11ac at 2.4 GHz and 5 GHz
3. Explore simulation of MAC layer rate adaptation algorithms 

# Performance Metrics and Modeling Scenarios
### Performance metrics
* Throughput
* Latency
* Packet error rate
* Range

### Models with simulation parameters
* Scenario 1: Aircraft stationary at different distances from an access point
    * Focus on standardized channel models for which verification is possible
* Scenario 2: Aircraft in motion towards the gate with a single access point
* Scenario 3: Aircraft in motion in taxi way covering multiple access points

# Methodology
* Step 1: Obtain PER vs. SNR plots for different MCSs 
    * Validate the simulation results by comparing it with results in standard documents
* Step 2: Obtain PER vs. distance plots for different EIRPs and noise floors
* Step 3: Develop rate adaptation algorithm and benchmark
* Step 4: Extend to Scenarios 2 and 3 
{{< figure src="/img/wifi/wifi-modelling-approach.png" >}}

## Data/plots generated and verification approach
* PER and throughput for different SNRs obtained for all MCSs
    * For 802.11n and 802.11ac 
    * Channel Models B, C, and D
* PER vs. SNR curves validated with those in _“Next Generation Wireless LANs,”_ E. Perahia and R. Stacey, Cambridge Univ. Press

{{< figure src="/img/wifi/Transmit-Receive-Sim.png" caption="Transmit-receive-chain simulation for an MCS" >}}

## Throughput calculation
* Given a distance, EIRP, noise floor, the SNR is calculated
* PER is obtained using the data generated for different MCS
* Throughput is calculated using the rate and PER
{{< figure src="/img/wifi/throughput-calc.png" caption="Throughput calculation" >}}

# Results
Throughputs were calculated for the following parameters:
* EIRP: 18 & 20 dBm
* Noise figures: 11, 13.5, 16 dB
* Bandwidth:  20 & 40 MHz for 11n, and 20, 40, 80 & 160 MHz for 11ac
* 1x1, 2x2, 3x3 & 4x4 antenna configurations
* Spatial streams: 1, 2, 3 & 4

## Throughput Results for IEEE 802.11n
{{< load-photoswipe >}}
{{< gallery dir="/img/wifi/802.11n_results" />}}
## Throughput Results for IEEE 802.11ac
{{< gallery dir="/img/wifi/802.11ac_results" />}}
## Validation
{{< figure src="/img/wifi/Validation.PNG" caption="Validation: PER vs. SNR: Model D, 802.11n" >}}

# Rate Adaptation Algorithms
* The goal is to develop an algorithm that chooses rate, number of spatial streams and bandwidth.  
* Several algorithms available in literature were studied:
    * Minstrel: Default in Linux.
    * MiRA (MIMO – Aware Rate Adaptation) 
    * RAMAS (Rate Adaptation for Multi-Antenna Systems)
    * Damysus
* We chose the Minstrel HT algorithm and started developing simulation scripts in MATLAB.

## Future
I actively contributed to the project until June 2021 after which I supported it part-time. For more details about this work on simulating Rate adaptation algorithms and
coexisting WLAN networks, [visit this page](https://labs.dese.iisc.ac.in/zenlab/ongoing-projects/wi-fi-modelling/). 

---

<!-- In-line html -->
<div style="text-align: right"> 
<a href="/projects">Back to Projects 👆</a>
</div>

<!-- #### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Shyam Sundar D G](http://linkedin.com/in/shyam-sundar-44216818a) -->

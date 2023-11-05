---
title: "Time Sensitive Networking Switch"
date: 2021-03-01
author: "Nithish K Gnani"
tags: [Networking, Tactile Internet]
categories: [Networking]
draft: false
---
---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: March 2021 - Present  
💰 Funded by: Ministry of Electronics and Information Technology (MeitY), Government of India and Center for Networked Intelligence (CNI), a Cisco CSR initiative.  
👩‍🏫 Guided by: [Chandramani Singh](https://faculty.dese.iisc.ac.in/chandramani/) and [TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/)  

---
_Note:_ This work is under progress. The information in this page is up to August 2022. The application developed over this work is detailed in the project "[Designing Tactile Cyber-Physical Systems](/project/tcps/)".

# Objective

1. To develop Time-Senstitive Networking (TSN) enabled ethernet switches on programmable network hardware (Netronome Agilio SmartNIC) using P4 programming language. To implement time synchronization in the network and then set up a TSN network. This involves implementing time aware shaper and gate control list at the switch ports.
2. To enable applications requiring ultra-reliable low latency communication (uRLLC) such as remote robotics assisted surgery.

{{< figure src="/img/tcps/TCPS_overview.jpg" caption="Overview of the project" >}}

## Modules:

Time-Sensitive Networking (TSN) switch (Towards implementing IEEE 802.1 TSN):
* Time Synchronization (Towards implementing IEEE 802.1AS)
* Time Aware Shaper (Towards implementing IEEE 802.1Qbv)
* Packet duplication and Elimination (Towards implementing IEEE. 802.1CB)
* Edge intelligent switch ports on programmable switches using P4



# Work Done

## Time synchronization

Implemented Precision Time Protocol (PTP) on Linux devices. Tested using four Raspberry Pi devices – R1, R2, R3, and R4. R3 is the grand-master clock using the Best Master Clock Algorithm (BMCA). The remaining devices are in slave configuration. Using software timestamping a sub 100 μs synchronization error was obtained.

{{< figure src="/img/tcps/TCPS_time_sync.jpg" caption="Time synchronization using PTP" >}}

## P4-based switch using Netronome Agilio SmartNIC

We have set up an ethernet switch using P4 programming language on the Netwronome Agilio SmartNIC. The match action table/rules contain the MAC addresses of the connected hosts. IP address is extracted from the packet and the packet is forwarded to a matching MAC address. The P4 program is also useful for obtaining and adding timestamps in a custom metadata header. Obtaining timestamps at the ports of the switch is a basic step for TSN.

{{< figure src="/img/tcps/TCPS_P4_switch.jpg" caption="P4 based switch using Netronome Agilio SmartNIC" >}}

## Time Aware Shaper (TAS) using LinuxTC on Netronome card

TSN is the IEEE 802.1Q defined standard technology to provide deterministic messaging on standard Ethernet. It provides guarantees of delivery and minimized jitter using time scheduling for those real-time applications that require determinism.
TAS is a feature specified in the IEEE 802.1Qbv standard that helps to guarantee bounded latency for time-critical frames in TSN by scheduling the transmission of frames within fixed intervals based on their priority.

{{< figure src="/img/tcps/TCPS_TAPRIO_implementation.jpg" caption="Implementation of TAPRIO" >}}
.

{{< figure src="/img/tcps/TCPS_TAPRIO_Results.jpg" caption="Results with cycle time of 20ms" >}}



# Ongoing and future work:

{{<figure src="/img/tcps/TCPS_future_work.jpg">}}


---

<!-- In-line html -->
<div style="text-align: right">
<a href="/project/tcps/">Go to Designing Tactile Cyber-Physical Systems 👆</a>
</div>

<!-- In-line html -->
<div style="text-align: right"> 
<a href="/projects">Back to Projects 👆</a>
</div>

#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Joydeep Pal](https://joygetsit.github.io/), [Deepak Choudhary](https://deepakc7y.github.io/)


---
title: "Designing Tactile Cyber-Physical Systems"
date: 2022-11-03T20:34:44+05:30
author: "Nithish K Gnani"
tags: [Networking, Tactile internet, robotics]
categories: [Networking]
draft: false
---


---

# Objective
_Design and implementation of a Tactile Cyber-Physical System for real-time interaction between physical and virtual worlds for applications requiring ultra-reliable low latency communication (uRLLC)._

To develop Time-Senstitive Networking (TSN) enabled ethernet switches on programmable network hardware (Netronome Agilio SmartNIC) using P4 programmikng language. To implement time synchronization in the network and then setup a TSN network. This involves implementing time aware shaper and gate control list at the switch ports.

To demonstrate a remote surgery scenario where a user with haptic device(s) can in real time perform complex tasks using a robotic arm at a remote location with no apparent experience of lag.

**Time-Sensitive Networking (TSN)** is the IEEE 802.1Q defined standard technology to provide deterministic messaging on standard Ethernet. It provides guarantees of delivery and minimized jitter using time scheduling for those real-time applications that require determinism.

{{< figure src="/img/tcps/TCPS_overview.jpg" caption="Overview of the TCPS project" >}}

## Modules:

1. Time-Senstitive Networking (TSN) switch (Towards implementing IEEE 802.1 TSN):
    * Time Synchronization (Towards implementing IEEE 802.1AS)
    * Time Aware Shaper (Towards implementing IEEE 802.1Qbv)
    * Packet duplication and Elimination (Towards implementing IEEE. 802.1CB)
2. Tactile Cyber-Physical System:
    * Real time control of a teleoperator robotic arm
    * Using haptic devices to send kinematic data and receive haptic feedback
    * Intelligence algorithms for performance improvement
    * Edge intelligent switch ports on programmable switches using P4



# Work Done
The work that has been completed in this project till date is described here.

[//]: # ({{< figure src="/img/tcps/TCPS_work_done.png" title="" >}})

## Time synchronization

Implemented Precision Time Protocol (PTP) on Linux devices. Tested using four Raspberry Pi devices – R1, R2, R3, and R4. R3 is the grand-master clock using the Best Master Clock Algorithm (BMCA). Remaining devices are in slave configuration. Using software timestamping a sub 100 μs synchronization error was obtained.

{{< figure src="/img/tcps/TCPS_time_sync.jpg" caption="Time synchronization using PTP" >}}

## P4 based switch using Netronome Agilio SmartNIC

We have setup a ethernet swtich using P4 programming language on the Netwronome Agilio SmartNIC. The match action table/rules contain the MAC addresses of the connected hosts. IP address is extracted from the packet and the packet is forwarded to a matching MAC address. The P4 program is also useful for obtaining and adding timestamp in a custom metadata header. Obtaining timestamps at the ports of the switch is a basic step for TSN.

{{< figure src="/img/tcps/TCPS_P4_switch.jpg" caption="P4 based switch using Netronome Agilio SmartNIC" >}}

## Time Aware Shaper using LinuxTC on Netronome card

{{< figure src="/img/tcps/TCPS_TAPRIO_implementation.jpg" caption="Implementation of TAPRIO" >}}
.

{{< figure src="/img/tcps/TCPS_TAPRIO_Results.jpg" caption="Results with cycle time of 20ms" >}}

## Feedback to the human operator

{{< figure src="/img/tcps/TCPS_force_feedback.gif" caption="Feedback felt by human using a Geomagic Touch haptic device from a simulated robotic arm in CoppeliaSim environment" >}}

## Control of UR3 robotic arm

UR3 from Universal Robots is a high precision capable collaborative robot. It comes with a patented programming interface – PolyScope. But it has no real time control capability. A Python program using rospy library was developed for real time control of the robot using its external control feature. Some issues of vibration and jerky motion was fixed by developing few algorithms.

{{< figure src="/img/tcps/TCPS_robot_motion.gif" caption="Eliminating vibrations and jerky motion" >}}

A demonstration of teleoperation of the UR3 robotic arm by a human operator using the Geomagic Touch haptic device:

{{< youtube id="JoljHneluBo" >}}





# Ongoing and future work:

{{<figure src="/img/tcps/TCPS_future_work.jpg">}}


---


#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Joydeep Pal](https://joygetsit.github.io/), [Deepak Choudary](https://deepakc7y.github.io/)
---
title: "Designing Tactile Cyber-Physical Systems"
date: 2022-03-01
author: "Nithish K Gnani"
tags: [Tactile Internet, Robotics]
categories: [Networking, Robotics]
draft: false
---
---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: March 2022 - Present  
💰 Funded by: Ministry of Electronics and Information Technology (MeitY), Government of India and Center for Networked Intelligence (CNI), a Cisco CSR initiative.  
👩‍🏫 Guided by: [Chandramani Singh](https://faculty.dese.iisc.ac.in/chandramani/) and [TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/)  

---
_Note:_ This work is under progress. The information in this page is up to August 2022.

# Objective

1. Design and implementation of a Tactile Cyber-Physical System for real-time interaction between physical and virtual worlds for applications requiring ultra-reliable low latency communication (uRLLC).  
2. To demonstrate a remote surgery scenario where a user with a haptic device(s) can in real time perform physical tasks using a robotic arm at a remote location.

{{< figure src="/img/tcps/TCPS_overview.jpg" caption="Overview of the TCPS project" >}}

## Modules:

* Using haptic devices to send kinematic data and receive haptic feedback
* Real-time control of a teleoperator robotic arm
* Intelligence algorithms for performance improvement
* Edge intelligent switch ports on programmable switches using P4



# Work Done

## Feedback to the human operator

{{< figure src="/img/tcps/TCPS_force_feedback.gif" caption="Feedback felt by a human using a Geomagic Touch haptic device from a simulated robotic arm in CoppeliaSim environment" >}}

## Control of UR3 robotic arm

UR3 from Universal Robots is a high-precision capable collaborative robot. It comes with a patented programming interface – PolyScope. But it has no real-time control capability. A Python program using rospy library was developed for real-time control of the robot using its external control feature. Some issues of vibration and jerky motion were fixed by developing a few algorithms.

{{< figure src="/img/tcps/TCPS_robot_motion.gif" caption="Eliminating vibrations and jerky motion" >}}

A demonstration of teleoperation of the UR3 robotic arm by a human operator using the Geomagic Touch haptic device:

{{< youtube id="JoljHneluBo" >}}

<!-- ## Edge-intelligent switch ports

{{< figure src="/img/tcps/TCPS_edge_Testbed-wide-v2.jpg" caption="Cyber-Physical System Testbed" >}} -->



# Ongoing and future work:

* Improving the performance and parallel processing using ROS2
* Developing application that utilizes haptic gloves to feel touch and grasp sensation while interacting with virtual and physical objects.


---

<!-- In-line html -->
<div style="text-align: right"> 
<a href="/projects">Back to Projects 👆</a>
</div>

#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Joydeep Pal](https://joygetsit.github.io/), [Deepak Choudhary](https://deepakc7y.github.io/)
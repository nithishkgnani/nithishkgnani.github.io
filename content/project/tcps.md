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
_Note:_ This work is under progress and the page will be updated.

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

## Interaction with Virtual Objects

{{< figure src="/img/tcps/TCPS-GT-OpenHaptics.png" caption="Using Geomagic Touch with OpenHaptics Toolkit" >}}

* You can feel the surface of the objects using the Geomagic Touch haptic device and move them around by holding the button.
* The haptic device freely moves when not touching the objects. When the object is touched, a force feedback is felt in normal to the surface of contact.
* At the end of the video, force is demonstrated by placing the pointer on top of the cube and then taking the force away by stopping the program.

{{< rawhtml >}}

<video width=100% controls yes>
    <source src="/img/tcps/GT_VR02.mp4" type="video/mp4">
    Interaction with VR.  
</video>

{{< /rawhtml >}}

## Force feedback from a simulated robot

* A simulated robot was built using Vrep/Coppelia Sim. You can control the position of end effector using Geomagic Touch
* When force feedback is enabled, it stops you from moving into virtual objects like the cube wall
* Time series plot of x-coordinate of the simulated robot and real Geomagic Touch shows that the robot cannot move beyond the cube wall.

{{< rawhtml >}}

<video width=100% controls yes>
    <source src="/img/tcps/SimRobot01.mp4" type="video/mp4">
    Force feedback from a simulated robot.  
</video>

{{< /rawhtml >}}

## Teleoperation of UR3 robotic arm

UR3 from Universal Robots is a high-precision capable collaborative robot. It comes with a patented programming interface – PolyScope. But it has no real-time control capability. A Python program using rospy library was developed for real-time control of the robot using its external control feature.  
Some issues of vibration and jerky motion were fixed by developing a few algorithms.

{{< rawhtml >}}

<video width=100% controls yes autoplay loop>
    <source src="/img/tcps/JerkyToSmooth02.mp4" type="video/mp4">
    Eliminating vibrations and jerky motion.  
</video>

{{< /rawhtml >}}

<!-- {{< figure src="/img/tcps/TCPS_robot_motion.gif" caption="Eliminating vibrations and jerky motion" >}} -->

A demonstration of teleoperation of the UR3 robotic arm by a human operator using the Geomagic Touch haptic device:

* Video feedback provided for inspecting the writing process
* A sense of floor touch would enhance and improve the experience

{{< youtube id="JoljHneluBo" >}}

## Force feedback - operating boundaries and floor touch

Applying force feedback to indicate breach of operating boundary and floor touch. This lead to easier and safer teleoperation of the robot for the writing task.

{{< rawhtml >}}

<video width=100% controls yes loop>
    <source src="/img/tcps/Boundary04.mp4" type="video/mp4">
    Operating boundary implementation.  
</video>

{{< /rawhtml >}}

# Ongoing and future work:

* Developed _pose correction_ algorithm that automatically adjusts the pose of a robot while gripping a tool.
* Developed _tremor suppression_ algorithm that suppresses tremors in the robot arm while controlling it using a haptic device.
* Improving the performance and parallel processing using ROS2
* Developing application that utilizes haptic gloves to feel touch and grasp sensation while interacting with virtual and physical objects.

{{< rawhtml >}}

<video width=100% controls yes autoplay loop>
    <source src="/img/tcps/GloveCalib01.mp4" type="video/mp4">
    SenseGlove Nova calibration.  
</video>

{{< /rawhtml >}}

---

<!-- In-line html -->
<div style="text-align: right">
<a href="/projects">Back to Projects 👆</a>
</div>

#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Joydeep Pal](https://joygetsit.github.io/), [Deepak Choudhary](https://deepakc7y.github.io/)
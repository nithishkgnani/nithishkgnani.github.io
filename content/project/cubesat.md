---
title: "Yaw Control of a CubeSat Using Reaction Wheels"
date: 2017-04-30
author: "Nithish K Gnani"
tags: [robotics, control, embedded systems]
categories: [robotics, control, embedded systems]
draft: true
---
---
🗺 Location: National Institute of Technology Karnataka, Surathkal, India  
📅 Duration: July 2016 - April 2017  
👩‍🏫 Bachelors major project, guided by [Prof. Prasad Krishna](https://mech.nitk.ac.in/faculty/prasad-krishna)  

---
<!-- EDIT THE VIDEO WITH TEXT INDICATORS AND TRY TO MUTE THE VOICE NARRATION -->

<!-- {{< rawhtml >}}

<video width=100% controls yes>
    <source src="/img/cubsat/CubeSat_video.mp4" type="video/mp4">
    Intercity haptic bilateral teleoperation.  
</video>

{{< /rawhtml >}} -->

# Objective

To implement a simple adaptive control algorithm, MRAC using the MIT rule, for yaw control of a suspended CubeSat body using a reaction wheel and compare it with PID control.

## Motivation and Summary

Space systems like satellites operate in complex and dynamic environments that require adaptive control strategies to cope with uncertainties and disturbances. The fixed gain PID controller cannot perfectly stabilize non-linear systems with uncertainties in terms of the model and parameters. An adaptive control algorithm can enhance the performance and provide the adaptive capability in such environments. One such strategy is model reference adaptive control (MRAC), which is used to design the controller that works by adjusting the controller parameters so that the output of the actual system tracks the output of a reference model having the same reference input. 

A reaction wheel is a type of flywheel used for orientation control of bodies, such as satellites, by changing its rotation speed and causing the body to counter-rotate proportionally through conservation of angular momentum

In this project, we implement a simple adaptive control algorithm using MRAC with the MIT rule for yaw control of a suspended body mimicking the yaw of a cubic satellite (CubeSat) using a reaction wheel. We compare our algorithm with PID control, which is a conventional feedback controller that uses proportional, integral, and derivative terms to adjust the parameters. We use SolidWorks to design and SimMechanics to simulate our system model. We also fabricate our physical CubeSat model using open source components.

{{< figure src="/img/cubesat/cubesat_physical_model.jpg" width=75% caption="Working model of a CubeSat" >}}

We did a comparison of the PID and MRAC controllers in terms of settling time, overshoot, and steady-state error. The MRAC controller shows better performance in the presence of uncertainties.

#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Dennis Joshy](https://www.linkedin.com/in/dmj6288/), [B Suresh](https://www.linkedin.com/in/b-suresh-09b4b562/)
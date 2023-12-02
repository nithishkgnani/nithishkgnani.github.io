---
title: "Yaw Control of a CubeSat Using Reaction Wheels"
date: 2017-04-30
author: "Nithish K Gnani"
tags: [robotics, control, embedded systems]
categories: [robotics, control, embedded systems]
draft: false
---
---
🗺 Location: National Institute of Technology Karnataka, Surathkal, India  
📅 Duration: July 2016 - April 2017  
👩‍🏫 Bachelor's thesis project, guided by [Prof. Prasad Krishna](https://mech.nitk.ac.in/faculty/prasad-krishna)  
📄 The detailed project report can be found in pdf format [here 🔗](/img/cubesat/CubeSat_Report_2017.pdf)

---

# Objective

To implement a simple adaptive control algorithm, MRAC using the MIT rule, for yaw control of a suspended CubeSat body using a reaction wheel and compare it with PID control.

{{< rawhtml >}}

<video width=100% controls yes>
    <source src="/img/cubesat/CubeSat02.mp4" type="video/mp4">
    Yaw control of a suspended CubeSat using a smartphone.  
</video>

{{< /rawhtml >}}


## Motivation and Summary

Space systems like satellites operate in complex and dynamic environments that require adaptive control strategies to cope with uncertainties and disturbances. The fixed gain PID controller cannot perfectly stabilize non-linear systems with uncertainties in terms of the model and parameters. An adaptive control algorithm can enhance the performance and provide the adaptive capability in such environments. One such strategy is model reference adaptive control (MRAC), which is used to design the controller that works by adjusting the controller parameters so that the output of the actual system tracks the output of a reference model having the same reference input. 

A reaction wheel is a type of flywheel used for orientation control of bodies, such as satellites, by changing its rotation speed and causing the body to counter-rotate proportionally through conservation of angular momentum

In this project, a simple adaptive control algorithm using MRAC with the MIT rule is implemented for yaw control of a suspended body mimicking the yaw of a cubic satellite (CubeSat) using a reaction wheel. This algorithm is compared with PID control, which is a conventional feedback controller that uses proportional, integral, and derivative terms to adjust the parameters. SolidWorks is used to design and SimMechanics to simulate the system model. Also a physical CubeSat model is fabricated using open source components.

A comparison of the PID and MRAC controllers is done in terms of settling time, overshoot, and steady-state error. The MRAC controller shows better performance in the presence of uncertainties.


{{< rawhtml >}}

<!-- Two images side by side with captions in html -->
<div style="display: flex; flex-direction: row; justify-content: space-between;">
    <figure>
        <img src="/img/cubesat/cubesat_cad_model.png" width=75%>
        <figcaption>CAD model of the CubeSat</figcaption>
    </figure>
    <figure>
        <img src="/img/cubesat/cubesat_physical_model.jpg" width=75%>
        <figcaption>Working model of the CubeSat</figcaption>
    </figure>
</div>

{{< /rawhtml >}}


---
**The detailed project report can be found in pdf format [here 🔗](/img/cubesat/CubeSat_Report_2017.pdf).**

---

<!-- In-line html -->
<div style="text-align: right"> 
<a href="/projects">Back to Projects 🔗</a>
</div>

<!-- #### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Dennis Joshy](https://www.linkedin.com/in/dmj6288/), [B Suresh](https://www.linkedin.com/in/b-suresh-09b4b562/), [Hari Shankar](https://www.linkedin.com/in/hari-shankar-s/) -->
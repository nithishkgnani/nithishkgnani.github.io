---
title: "Projects"
date: 2022-10-30T19:05:33+05:30
draft: true
---

<div style="text-align: justify"> 

{{< rawhtml >}}

<h3>Cyber-Physical Systems and Tactile Internet</h3>

<div style="display: flex; align-items: center;">
    <div style="flex: 40%;">
        <img src="/img/project_tiles/TCPS_testbed.png" >
    </div>
    <div style="flex: 60%;">
        <h5>&nbsp;&nbsp;&nbsp;&nbsp;Designing Tactile Cyber-Physical Systems (TCPS)</h5>
        <ul>
            <li>Designed and executed a Tactile Cyber-Physical System (TCPS) connecting a haptic device and a robotic arm for live teleoperation.</li>
            <li>Developed <i>pose correction</i> algorithm that automatically adjusts the pose of a robot while gripping a tool.</li>
            <li>Developed <i>tremor suppression</i> algorithm that suppresses tremors in the robot arm while controlling it using a haptic device.</li>
            <li><a href="/project/tcps/">Detailed project page 🔗</a></li>
        </ul>
    </div>
</div>
<!-- <hr> -->

<div style="display: flex; align-items: center;">
    <div style="flex: 40%;">
        <img src="/img/project_tiles/1_tsn-switch.png" >
    </div>
    <div style="flex: 60%;">
        <h5>Time Sensitive Networking (TSN) switch</h5>
        Built an IEEE 802.1 TSN-capable ethernet switch with hardware implementation of time synchronization (IEEE 802.1AS), Time Aware Shaper (IEEE 802.1Qbv), and packet duplication/elimination (IEEE 802.1CB). Key novelties:
    </div>
</div>
<ul>
    <li><i>µTAS</i> - Employed P4-MicroC-based design for SmartNIC, enabling Time-Aware Shaper offloading and achieving a 20 µs latency between connected hosts via SmartNICs.</li>
    <li>Devised packet de-duplication algorithms for SmartNICs, bolstering Scheduled Traffic reliability. Attained 100% packet delivery at destination for a single 2.5 Gbps stream across two links with 10% losses each. Achieved 99.88% efficiency & 99.83% packet delivery for 12 simultaneous streams.</li>
    <li><i>EdgeP4</i> - Embedding intelligence for <i>pose correction</i> and <i>tremor suppression</i> in P4-programmable edge switches. These algorithms curbed control loop latency (<100µs) and network load (99% reduction), demonstrating versatility in algorithm-switching for distinct tasks via P4's match-actions.</li>
    <li><a href="/project/tsn/">Detailed project page 🔗</a></li>
</ul>
<!-- <hr> -->

<div style="display: flex; align-items: center;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/9_CubeSat.png" >
    </div>
    <div style="flex: 70%;">
        <h5>Yaw control of a CubeSat using reaction wheels</h5>
        Designed a suspended CubeSat body and achieved precise control of its yaw using reaction wheels using a manually tuned PID controller. Modeled it in Simulink and implemented Model Reference Adaptive Control (MRAC) using the MIT rule and achieved better performance compared to PID control.<br>
        <a href="/project/cubesat/">Detailed project page 🔗</a>
    </div>
</div>
<hr>

<h3>IoT data management, indoor localization and security</h3>


<div style="display: flex; align-items: center;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/2_Acoustic-Localization2.png" >
    </div>
    <div style="flex: 70%;">
        <h5>&nbsp;&nbsp;&nbsp;&nbsp;Acoustics Based Localization</h5>
        <ul>
            <li>Developed an application to locate multiple wireless edge devices with embedded microphones by using audio signals from speakers. </li>
            <li>Simulated a few localization algorithms using MATLAB. Implemented KNN fingerprinting based localization of the receivers and achieved an accuracy of 98%.</li>
            <li><i>Novelty:</i> Unlike the usual source localization, here, the receivers (mics) are localized when the locations of speakers are known.</li>
            <li><a href="/project/acoustic-localization/">Detailed project page 🔗</a></li>
        </ul>
    </div>
</div>
<!-- <hr> -->

<div style="display: flex; align-items: center;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/3_AIOT-Data-Management.png" >
    </div>
    <div style="flex: 70%;">
        <h5>&nbsp;&nbsp;&nbsp;&nbsp;Airplane IoT data analytics and management</h5>
        <ul>
            <li>Developed machine learning algorithms to classify anomalies and take corrective actions using real-time data generated from sensors from a MATLAB/Simulink model of an aircraft environmental control system. </li>
            <li><i>Novelty:</i> Developed an algorithm that does linear interpolation between non-consecutive data points from time series data to adaptively store data based on a cost function which balances storage space savings and error in reconstruction of data. Achieved 96% savings in storage space.</li>
            <li><a href="/project/aiot/">Detailed project page 🔗</a></li>
        </ul>
    </div>
</div>
<hr>


<h3>Wireless communication and video streaming</h3>
<div style="display: flex; align-items: center;">
    <div style="flex: 40%;">
        <img src="/img/project_tiles/4_WLAN-Modelling.png" >
    </div>
    <div style="flex: 60%;">
        <h5>&nbsp;&nbsp;&nbsp;&nbsp;Wi-Fi Modelling</h5>
        <ul>
            <li>Modelling & simulation of IEEE 802.11n & 802.11ac using MATLAB. </li>
            <li>Performance Metrics: throughput, packet error rate & range.</li>
            <li>Implementing Rate Control Algorithms in MATLAB. </li>
            <li><a href="/project/wi-fi-modelling/">Detailed project page 🔗</a></li>
        </ul>
    </div>
</div>


<div style="display: flex; align-items: center;">
    <div style="flex: 35%;">
        <!-- <img src="/img/project_tiles/5_AMMAZING.png" > -->
        <iframe src="https://www.youtube.com/embed/QhCendre_SY" title="5G-AMMAZING-summary" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div style="flex: 65%;">
        <h5>&nbsp;&nbsp;&nbsp;&nbsp;5G - AMMAZING</h5>
        <ul>
            <li>An end to end 5G mmWave system for infotainment. </li>
            <li><i>Novelty:</i> Data & control plane of a video stream split over 5G and regular Wi-Fi.</li>
            <li>Won first place and a cash award of $13,200 in 5G Hackathon 2020 by Govt. of India </li>
            <li><a href="/project/5g-ammazing/">More details 🔗</a></li>
        </ul>
    </div>
</div>
<!-- <hr> -->

<div style="display: flex; align-items: center;">
    <div style="flex: 35%;">
        <img src="/img/project_tiles/6_Video-Casting.gif" >
    </div>
    <div style="flex: 65%;">
        <h5>&nbsp;&nbsp;&nbsp;&nbsp;Video casting</h5>
        <ul>
            <li>As 2.4 & 5 GHz Wi-Fi is congested in an aircraft cabin in which 400+ passengers cast media onto seat back displays in close proximity, using IEEE 802.11ad, 60GHz Wi-Fi (Wi-Gig) & 802.11ax (Wi-Fi 6E) was explored.</li>
            <li>MATLAB WLAN Toolbox was used to simulate the physical behavior of Wi-Fi transmissions in a dense environment.</li>
            <li><i>Novelty:</i> Developed an algorithm that dynamically allocates different channels to 400 transmitters such that the packet error ratio is zero (PER = 0).</li>
            <li><a href="/project/video-casting/">More details 🔗</a></li>
        </ul>
    </div>
</div>
<hr>


<h3>Hobby projects</h3>

<div style="display: flex; align-items: center;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/8_3D-prints.png" width=95%>
    </div>
    <div style="flex: 70%;">
        <h5>Designing 3D printed products</h5>
        Designing and 3D printing figurines, models and functional products for home and work.<br>
        <a href="/project/3d-prints/">Link to the products developed 🔗</a>
    </div>
</div>
<!-- <hr> -->

<div style="display: flex; align-items: center;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/7_Nitro-plane.jpg" width=95%>
    </div>
    <div style="flex: 70%;">
        <h5>Building and flying RC planes</h5>
        Built RC planes using balsa wood, biofoam and corrugated plastic sheets, powered by brushless motors and nitro engines. Won flying competitions in Mangalore region. Conducted RC plane building workshops.<br>
        <a href="/project/rc-planes/">Link to the planes built 🔗</a>
    </div>
</div>

{{< /rawhtml >}}

</div>
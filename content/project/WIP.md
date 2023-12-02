---
title: "Projects"
date: 2022-10-30T19:05:33+05:30
draft: true
---

<div style="text-align: justify"> 

## Cyber-Physical Systems and Tactile Internet 

{{< rawhtml >}}

<div style="display: flex;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/TCPS_testbed.png" >
    </div>
    <div style="flex: 70%;">
        <h3>Designing Tactile Cyber-Physical Systems (TCPS)</h3>
        <ul>
            <li>Designed and executed a Tactile Cyber-Physical System (TCPS) connecting a haptic device and a robotic arm for live teleoperation.</li>
            <li>Developed <i>pose correction</i> algorithm that automatically adjusts the pose of a robot while gripping a tool.</li>
            <li>Developed <i>tremor suppression</i> algorithm that suppresses tremors in the robot arm while controlling it using a haptic device.</li>
            <li><a href="/project/tcps/">Detailed project page 🔗</a></li>
        </ul>
    </div>
</div>

{{< /rawhtml >}}


---

<div style="display: flex;">
    <div style="flex: 30%;">
        <img src="/img/project_tiles/TCPS_testbed.png" >
    </div>
    <div style="flex: 70%;">
        <h3>Time Sensitive Networking (TSN) switch</h3>
        <ul>
            <li>Designed and executed a Tactile Cyber-Physical System (TCPS) connecting a haptic device and a robotic arm for live teleoperation.</li>
            <li>Developed <i>pose correction</i> algorithm that automatically adjusts the pose of a robot while gripping a tool.</li>
            <li>Developed <i>tremor suppression</i> algorithm that suppresses tremors in the robot arm while controlling it using a haptic device.</li>
            <li><a href="/project/tcps/">Detailed project page 🔗</a></li>
        </ul>
    </div>
</div>

{{< /rawhtml >}}

{{< details "**Time Sensitive Networking (TSN) switch** " open >}}

![](/img/project_tiles/1_tsn-switch.png "TCPS and TSN overview")

Built an IEEE 802.1 TSN-capable ethernet switch with in-hardware implementation of time synchronization (IEEE 802.1AS), Time Aware Shaper (IEEE 802.1Qbv), and packet duplication/elimination (IEEE 802.1CB). Key novelties:
1. _P4TAS_ - Employed P4-based design for SmartNIC, enabling Time-Aware Shaper offloading and achieving a 20 µs latency between connected hosts via SmartNICs.
2. Devised packet de-duplication algorithms for SmartNICs, bolstering Scheduled Traffic reliability. Attained 100% packet delivery at destination for a single 2.5 Gbps stream across two links with 10% losses each. Achieved 99.88% efficiency & 99.83% packet delivery for 12 simultaneous streams.
3. _EdgeP4_ - Embedding intelligence for _pose correction_ and _tremor suppression_ in P4-programmable edge switches. These algorithms curbed control loop latency (<100 µs) and network load (99% reduction), demonstrating versatility in algorithm-switching for distinct tasks via P4's match-actions.

[🔗 More details](/project/tsn/)  
{{< /details >}}

---
{{< details "**Yaw control of a CubeSat using reaction wheels** " open >}}

![](/img/project_tiles/9_CubeSat.png "Yaw control of CubeSat using reaction wheels")

* Designed a suspended CubeSat body and achieved precise control of its yaw using reaction wheels using a manually tuned PID controller.
* Modeled it in Simulink and implemented Model Reference Adaptive Control (MRAC) using the MIT rule and achieved better performance compared to PID control.

[🔗 More details](/project/cubesat/)  
{{< /details >}}

## IoT data management, indoor localization and security  

{{< details "**Acoustics Based Localization**" open >}}

![](/img/project_tiles/2_Acoustic-Localization2.png "Localization setup")

* Developed an application to locate multiple wireless edge devices with embedded microphones by using audio signals from speakers. 
* Simulated a few localization algorithms using MATLAB. Implemented KNN fingerprinting based localization of the receivers and achieved an accuracy of 98%.
* _Novelty:_ Unlike the usual source localization, here, the receivers (mics) are localized when the locations of speakers are known.
Developed an application to locate multiple wireless edge devices with embedded microphones by using audio signals from speakers.  

[🔗 More details](/project/acoustic-localization/) 
{{< /details >}}

---
{{< details "**Airplane IoT data analytics and management**" open >}}

![](/img/project_tiles/3_AIOT-Data-Management.png "AIOT data management")

* Developed machine learning algorithms to classify anomalies and take corrective actions using real-time data generated from sensors from a MATLAB/Simulink model of an aircraft environmental control system.
* _Novelty:_ Developed an algorithm that does linear interpolation between non-consecutive data points from time series data to adaptively store data based on a cost function which balances storage space savings and error in reconstruction of data. Achieved 96% savings in storage space. 

[🔗 More details](/project/aiot/) 
{{< /details >}}

## Wireless communication and video streaming  

{{< details "**Wi-Fi Modelling**" open >}}

![](/img/project_tiles/4_WLAN-Modelling.png "WLAN modelling in MATLAB")

* Modelling \& simulation of IEEE 802.11n \& 802.11ac using MATLAB. 
* Performance Metrics: throughput, packet error rate \& range.
* Implementing Rate Control Algorithms in MATLAB. 

[🔗 More details](/project/wi-fi-modelling/) 
{{< /details >}}

---
{{< details "**5G - AMMAZING – Advanced MM-wAve Systems for Informatics at Gigabit**" open >}}

![](/img/project_tiles/5_AMMAZING.png "5G - AMMAZING - Overview")

* An end to end 5G mmWave system for infotainment.
* _Novelty:_ Data \& control plane of a video stream split over 5G and regular Wi-Fi.
* Shortlisted in top 10 teams in 5G Hackathon 2020-22 by Department of Telecommunication (DoT), Government of India. 

[🔗 More details](/project/5g-ammazing/)
{{< /details >}}

---
{{< details "**Video casting**" open >}}

![](/img/project_tiles/6_Video-Casting.gif "Wi-Fi channel interference in an aircraft cabin")

* Passengers bring media content on personal portable devices onto an airplane, and desire to “cast” the media onto seat back displays in an aircraft cabin.
* Considering that 2.4 \& 5 GHz Wi-Fi is congested in an aircraft cabin in which 400+ passengers use devices to cast media onto seat back displays in close proximity, the possibility of using IEEE 802.11ad, 60GHz Wi-Fi (Wi-Gig) \& 802.11ax (Wi-Fi 6E) was explored.
* WLAN Toolbox in MATLAB was used to simulate the physical behavior of Wi-Fi transmissions in a dense environment.
* _Novelty:_ Developed an algorithm that dynamically allocates different channels to 400 transmitters such that the packet error ratio is zero (PER = 0). 

[🔗 More details](/project/video-casting/)
{{< /details >}}


## Hobby projects  

{{< details "**Designing 3D printed products**" open >}}

![](/img/project_tiles/8_3D-prints.png "3D printed products")

* Designing and 3D printing figurines, models and functional products for home and work.

[🔗 More details](/project/3d-prints/)
{{< /details >}}

---
{{< details "**Building and flying RC planes**" open >}}

![](/img/project_tiles/7_Nitro-plane.jpg "RC Planes")

* Built RC planes using balsa wood, biofoam and corrugated plastic sheets, powered by brushless motors and nitro engines.
* Won flying competitions in Mangalore region. 
* Conducted RC plane building workshops.

[🔗 More details](/project/rc-planes/)
{{< /details >}}

</div>
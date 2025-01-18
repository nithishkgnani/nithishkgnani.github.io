---
title: "FPV Goggles"
date: 2024-05-25T20:43:59+05:30
author: "Nithish K Gnani"
tags: [Tactile Internet, design, product development]
categories: [Networking, design, product development]
draft: false
---

---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: February 2024 - August 2024  
🤝 For: National Hub for Healthcare Instrumentation Development, India.  
👩‍🏫 Collaborators: [Prof. TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/) and [Dr. Senthilvelan Rajagopalan](https://www.linkedin.com/in/senthilvelan-rajagopalan-89904a78)  

---

### Motivation

In February 2024, I met Dr. Senthilvelan, arthroscopic surgeon (shoulder, elbow, wrist). He was looking for a solution to record and stream live video from the surgery room for reference and training. The doctor can wear first person view (FPV) goggles which can record and stream the live video to a server. The existing solutions were bulky and expensive. I decided to design a lightweight and affordable FPV goggles.

### Design

The FPV goggle is in a regular spectacle frame form factor. It houses a Nicla Vision at the nose bridge. It is an embedded board with a STM32H747AII6 Dual ARM® Cortex® M7/M4 IC processor, 2MP camera, microphone, and wireless connectivity. It is 23mm x 23mm in size and fits on the nose bridge without obstructing the view.
It is coded to stream live video over WiFi. Various methods of streaming are being tested like UDP, HTTP and RTSP.

#### Preliminary design

In this design, the Nicla Vision is powered by a battery that is carried in the pockets of the user. I worked on an improved design that integrates the battery wiring into the spectacle frame.

{{<figure src="/img/fpv-goggles/specs-v1.png" caption="Preliminary design">}}

<!-- {{< rawhtml >}}
<div style="display: flex; align-items: center;">
    <div style="flex: 50%;">
        <img src="/img/fpv-goggles/specs-v1-components.jpg" width=75%>
    </div>
    <div style="flex: 50%;">
        <img src="/img/fpv-goggles/specs-v1-assembled.jpg" width=75%>
    </div>
</div>
{{< /rawhtml >}} -->

A sample video stream from the FPV goggles in operation is shown below.  
{{< rawhtml >}}
<video width=50% controls yes>
    <source src="/img/fpv-goggles/Nicla-specs-01.mp4" type="video/mp4">
    Live video stream from the FPV goggles.
</video>
{{< /rawhtml >}}

#### Battery life
I tested the battery life. At this video quality, a 500mAh LiPo battery can run the video stream for 3 hours. 

#### Battery integration and pause switch

In this design, the battery is integrated into the spectacle frame and is comfortable held at the back of the head using a 3D printed holder.  In this design, I used a 5000mAh power bank as it is commercially available and easy to charge using USB. On full charge, the FPV goggles can stream for well above 10 hours. A switch is integrated into the spectacle frame that is slid to turn on and off the streaming. There is also a spring loaded screw to adjust the camera angle as per the user's comfort.

{{<figure src="/img/fpv-goggles/specs-v6.png" caption="Spring loaded screw to adjust the camera angle">}}

{{< rawhtml >}}
<video width=70% controls yes>
    <source src="/img/fpv-goggles/Nicla-specs-02.mp4" type="video/mp4">
    Battery on frame and pausing the video.
</video>
{{< /rawhtml >}}

A snapshot of the CAD design of the spectacle frame is shown below. I desigend it to be printed in multiple parts and then assembled as my 3D printer is a basic one and cannot handle intricate prints.
{{<figure src="/img/fpv-goggles/specs_design.png" caption="CAD Design of the frame">}}

### Future work

I left the project in August 2024 as I moved to Europe. The project is continued by lab team at IISc. The goal is to use thinner wires and integrate the battery inside the spectacle frame by using smaller batteries depending on how long a stream needs to be.

---

<!-- In-line html -->
<div style="text-align: right"> 
<a href="/projects">Back to Projects 🔗</a>
</div>
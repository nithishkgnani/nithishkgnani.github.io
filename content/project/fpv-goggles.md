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
📅 Duration: February 2024 - Present  
🤝 For: National Hub for Healthcare Instrumentation Development, India.  
👩‍🏫 Collaborators: [Prof. TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/) and [Dr. Senthilvelan Rajagopalan](https://www.facebook.com/Senthilvelan.Rajagopalan)  

---
_Note:_ This work is under progress and the page will be updated with newer designs.

### Motivation

In February 2024, I met Dr. Senthilvelan, arthroscopic surgeon (shoulder, elbow, wrist). He was looking for a solution to record and stream live video from the surgery room for reference and training. The doctor can wear first person view (FPV) goggles which can record and stream the live video to a server. The existing solutions were bulky and expensive. I decided to design a lightweight and affordable FPV goggles.

### Design

The FPV goggle is in a regular spectacle frame form factor. It houses a Nicla Vision at the nose bridge. It is an embedded board with a STM32H747AII6 Dual ARM® Cortex® M7/M4 IC processor, 2MP camera, microphone, and wireless connectivity. It is 23mm x 23mm in size and fits on the nose bridge without obstructing the view.
It is coded to stream live video over WiFi. Various methods of streaming are being tested like UDP, HTTP and RTSP.

#### Preliminary design

Currently, the Nicla Vision is power by a battery that is carried in the pockets of the user. I'm working on a better design that integrates the battery wiring into the spectacle frame.

{{< rawhtml >}}
<div style="display: flex; align-items: center;">
    <div style="flex: 50%;">
        <img src="/img/fpv-goggles/specs-v1-components.jpg" width=95%>
    </div>
    <div style="flex: 50%;">
        <img src="/img/fpv-goggles/specs-v1-assembled.jpg" width=95%>
    </div>
</div>
{{< /rawhtml >}}

A sample video stream from the FPV goggles in operation is shown below.  
{{< rawhtml >}}
<video width=50% controls yes>
    <source src="/img/fpv-goggles/Nicla-specs-01.mp4" type="video/mp4">
    Live video stream from the FPV goggles.
</video>
{{< /rawhtml >}}
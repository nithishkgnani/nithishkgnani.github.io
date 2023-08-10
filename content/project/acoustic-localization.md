---
title: "Acoustic Localization"
date: 2023-08-10T18:53:40+05:30
author: "Nithish K Gnani"
tags: [indoor localization, embedded, aerospace]
categories: [Aerospace network]
draft: false
---
---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: March 2019 - February 2020  
💰 Funded by: Boeing  
👩‍🏫 Guided by: [Dr. Chandramani Singh](https://faculty.dese.iisc.ac.in/chandramani/) and [Dr. TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/)  

---

# Objective
_To develop an application that maps the physical location of multiple wireless end devices (with embedded miniature microphones) by using audio signals from two rows of individually addressable speakers._

{{< figure src="/img/al/al-cabin.png" >}}

## Work Done
During pre-boarding checks in an aircraft articles/assets such as safety vests are checked to be in place in the aircraft cabin. The task was to automate this process by leveraging the cabin announcement speakers. Four speakers were connected to a nRF52840 development board and programmed to beep in a sequence. A custom embedded board using Nordic nRF52840 microcontroller was designed and developed in my lab with four ADC inputs. A Microphone was connected to it. The node was programmed to measure the time between audio pulses arriving from different speakers. Such nodes were placed under the seats in a mock aircraft cabin setup to test various localization algorithms to detect whether under-seat life safety vests are in their place. 

{{< load-photoswipe >}}
{{< gallery dir="/img/al/al-gallery1" />}}

### Localization Algorithms Simulated in MATLAB
1. RSS based spherical intersection (3D lateration) 
2. TDoA based spherical intersection 
3. TDoA based angle estimation

{{< figure src="/img/al/al-SX.png" >}}
{{< figure src="/img/al/al-TDoA_Angle.png" >}}

### Fingerprinting TDoA
It was observed that a complex space like an aircraft cabin has no direct path between the speakers and microphones for sound to travel. This makes accurate measurement of the time between the arrival of beeps very difficult with the need to develop complicated algorithms. Our solution is low compute and energy efficient. We fingerprint the time difference between the arrival of sound from different speakers and use KNN algorithm to determine the location of a node.
{{< figure src="/img/al/al-Fingerprinting.png" >}}


### Demonstration
The sequence of steps involved in localizing the node can be seen in the video below. A smartphone running an Android application sends a command to the speaker controller board using BLE. The speakers beep successively. The nodes measure the time difference between the arrival of these beeps. The time information is communicated back to the smartphone. The application runs the KNN algorithm to determine if the nodes (hence the safety vests) are in their place.

{{< youtube id="ZKtaTy-hZzg" >}}
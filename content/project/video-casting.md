---
title: "Video Casting in Dense Wi-Fi"
date: 2020-02-01
author: "Nithish K Gnani"
draft: false
---
---
🗺 Location: Indian Institute of Science (IISc), Bangalore, India  
📅 Duration: February 2020 - January 2021  
💰 Funded by: Boeing  
👩‍🏫 Guided by: [Prof. TV Prabhakar](https://labs.dese.iisc.ac.in/zenlab/people/tv-prabhakar/)  

---

# Problem Statement
* Passengers bring media content on personal portable devices onto an airplane, and it is desirable to “cast” onto seat back displays.
* Considering that 2.4 & 5 GHz Wi-Fi on an airplane is congested, desirable to leverage alternate technology that is/will be supported in COTS portable devices.
* Develop a wireless casting solution that
    * supports high-resolution (4K) video bandwidth
    * scales to 400+ passenger devices in close proximity. 

{{< figure src="/img/vid-cast/cabin-layout.jpg" caption="Cabin layout in Boeing 777-9">}}

### Desired features of the solution:
* High-resolution (4K) video bandwidth
* 400+ passenger devices in an aircraft cabin
* No interference between devices of passengers in close proximity
* Video Casting or Screen Mirroring Options

# Summary
* A document  was prepared with market survey and casting methods available in wired and wireless casting. 
* Since 2.4 \& 5 GHz Wi-Fi is congested in an aircraft cabin, the possibility of using IEEE 802.11ad, 60GHz Wi-Fi (Wi-Gig) \& 802.11ax (Wi-Fi 6E) was explored.
* WLAN Toolbox in MATLAB was used to simulate the physical behavior of Wi-Fi transmissions in a dense environment.
* Developed an algorithm that dynamically allocates different channels to 400 transmitters such that the packet error ratio is zero (PER = 0). 

## Key takeaways from 802.11ad, Wi-Gig study
Considering the simulations performed and observations made, we find the following key takeaways from the study made for 802.11ad while testing for 400 seats in a cabin environment -
* When the Tx is placed in the food tray, MCS 2 (π/2-BPSK modulation) would be able to transmit 4K Video with good through put and PER <= 10% in all channels for 400 seats 
* When Tx is placed in the Lap position, MCS 2 would still be able to transmit 4K Video with good throughput and PER <=10%. Higher MCS such as MCS 6 and above shall experience PER > 10% in this condition. 
* Modulation schemes 7 and above may not be suitable for transmitting 4K videos in cabin environment for 400 seats as they may experience > 10% PER in the conditions specified.

{{< figure src="/img/vid-cast/wigig-sim-params.jpg" caption="Wi-Gig simulation scenario">}}

## Key takeaways from 802.11ax, Wi-Fi 6E study
* Most mobile phones have TxPower in around 11 dBm
* MCS 3 and above can support 4K videos of 25 Mbps bit rate transmission 
* As transmission power increases, the packet error ratio (PER) drops. Window seats have lower PERs.  
(best-PER = 0; worst PER = 1)
    {{< figure src="/img/vid-cast/Result_tx-pow.jpg">}}
* As receiver antenna gain increases, PER drops.
    {{< figure src="/img/vid-cast/Result_rx-gain.jpg">}}

## Channel allocation algorithm
* 59 non overlapping 20MHz channels of Wi-Fi 6E are used to simulate the events inside the cabin.
* All the Wi-Fi nodes are active simultaneously and we aim for a channel matrix that gives the lowest PER.

{{< figure src="/img/vid-cast/Algo-ch-alloc.png" caption="AP channel allocation algorithm">}}
</br> <!--  Extra vertical space -->
{{< figure src="/img/vid-cast/VC_animation.gif" caption="Tx-Rx Link and Interference">}}

### Result
##### Channel allocation across all 400 seats converges to PER = 0
* With independent access points, the channel allocation procedure will repeat every time the usage scenario changes.
* By using WLAN controllers the allocation procedure will need to run only once as after that, all the APs can be set to suitable channels.
* Virtual WLAN controllers like OpenWISP, Chillispot could be used to automate several aspects of network deployment and management.

{{< figure src="/img/vid-cast/Result-algo-ch-alloc.png" caption="Channel allocation on 400 seats and resulting PER">}}

## Video casting study document
The document is a comprehensive and informative guide on video casting and its various aspects. It provides useful insights and recommendations for anyone interested in video casting technology.
- Wireless casting: The document explains how wireless casting works using Wi-Fi standards, such as 802.11ad and 802.11ay, and their advantages and disadvantages for video casting. It also discusses the possibility of using private LTE networks for video casting.
- Casting method: The document compares different methods of video casting, such as DLNA, WebRTC, and HDMI-CEC. It describes the underlying stack, pros and cons, and use cases of each method. It also proposes a video casting architecture using WebRTC and its components.
- Streaming protocols: The document reviews different streaming protocols that are used for video casting, such as RTSP/RTP, RTMP, HLS, and MPEG-DASH. It evaluates their performance, compatibility, and features.
- Wired casting: The document explores different wired casting options, such as HDMI, DisplayPort, USB Type-C, and MHL. It explains how they work, what connections they support, and what features they offer.
- Solutions available in the market: The document lists some of the existing solutions that provide video casting capabilities, such as Chromecast, Roku, Apple TV, Amazon Fire TV, Miracast, AirPlay, and WiDi. It compares their features, compatibility, and pricing.





---

<!-- In-line html -->
<div style="text-align: right"> 
<a href="/projects">Back to Projects 👆</a>
</div>

#### Team
[Nithish K Gnani](https://nithishkgnani.github.io/), [Pratyush Shukla](https://www.linkedin.com/in/pratyush-shukla/%20%20)

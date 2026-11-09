---
title: "Home"
date: 2026-11-09
draft: false
---

<div class="video-showcase">
  <video autoplay loop muted playsinline class="featured-video">
    <source src="/img/project_tiles/portrait/Teleop_vid_short.mp4" type="video/mp4">
  </video>
</div>

<div class="bio-intro">
  <p>
    I am an engineer and researcher working at the intersection of <strong>Cyber-Physical Systems (CPS)</strong>, <strong>Robotics</strong>, <strong>Real-Time Control</strong>, and <strong>Mechatronics</strong>. I hold a dual M.Sc. in Autonomous Systems from <strong>KTH Royal Institute of Technology</strong> (Sweden) and <strong>Polytech Nice Sophia, Université Côte d'Azur</strong> (France), backed by a B.Tech in Mechanical Engineering from <strong>NITK Surathkal</strong>.
  </p>
  <p>
    Most recently, I completed my master's thesis and R&D work at <strong>Scania (TRATON Group)</strong> in Sweden, developing machine learning models and closed-loop simulator-based driver-support policies over 20,000+ hours of commercial battery-electric truck telemetry. Previously, I spent 5.5 years as a researcher at the <strong>Indian Institute of Science (IISc)</strong> in the Centre for Networked Intelligence (<a href="https://cni.iisc.ac.in/">CNI</a>) and DESE, leading projects across bounded-latency robotic teleoperation, in-network computing on P4 programmable switches, Time-Sensitive Networking (TSN), and rapid mechatronic prototyping.
  </p>
</div>

---

<h2 id="projects">Featured Projects and Builds</h2>

<p class="section-intro">Selected engineering and research builds across robotics, programmable networking, haptics, and mechatronics. Click any project for architecture details, schematics, and demonstrations.</p>

<div class="projects-grid">

  <!-- RoboTwin Card -->
  <div class="project-card">
    <img class="project-thumbnail" src="/img/robotwin/known-object.png" alt="RoboTwin Framework" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">Digital Twins</span>
        <span class="tag-badge">Robotics</span>
        <span class="tag-badge">Teleoperation</span>
      </div>
      <h3 class="project-title"><a href="https://arxiv.org/pdf/2506.01027" target="_blank" rel="noopener">RoboTwin</a></h3>
      <p class="project-desc">
        A dual-digital-twin teleoperation framework synchronizing physical manipulators with GPU-accelerated NVIDIA Isaac Sim and ROS2. The operator-side twin provides zero-latency haptic feedback via Geomagic Touch, while the remote twin validates safe operating bounds before physical execution. Using RealSense RGB-D vision, YOLOv8 object detection, and SSIM discrepancy tracking, it streams semantic state updates—cutting network bandwidth by 25x and reducing NASA-TLX cognitive workload.
      </p>
      <a class="project-link-btn" href="https://arxiv.org/pdf/2506.01027" target="_blank" rel="noopener">View Preprint &rarr;</a>
    </div>
  </div>

  <!-- EdgeP4 Card -->
  <div class="project-card">
    <img class="project-thumbnail" src="/img/project_tiles/landscape/TCPS_testbed.png" alt="EdgeP4 Testbed" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">P4</span>
        <span class="tag-badge">Edge Intelligence</span>
        <span class="tag-badge">SmartNIC</span>
        <span class="tag-badge">TSN</span>
      </div>
      <h3 class="project-title"><a href="/project/tcps/">EdgeP4</a></h3>
      <p class="project-desc">
        In-network computing framework running directly on P4-programmable switches and Netronome Agilio SmartNICs to overcome host-side OS jitter in wide-area robotics. Offloads tremor suppression and closed-loop pose correction into the network data plane, slashing feedback latency below 100 µs and cutting wide-area network traffic by up to 99.9%. Validated on an intercity tactile CPS testbed across 400 km with a UR3 manipulator. Awarded Best Paper at IEEE INFOCOM CNERT 2024.
      </p>
      <a class="project-link-btn" href="https://github.com/nithishkgnani/EdgeP4">Code &rarr;</a>
      <a class="project-link-btn" href="/project/tcps/">Project Details &rarr;</a>
    </div>
  </div>

  <!-- Embodied Card -->
  <div class="project-card">
    <img class="project-thumbnail" src="/img/social-robotics/user-study-setup.jpg" alt="Embodied Furhat Robot ASL Interpreter" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">Social Robotics</span>
        <span class="tag-badge">HRI</span>
        <span class="tag-badge">Computer Vision</span>
      </div>
      <h3 class="project-title"><a href="/project/asl-robot-interpreter/">Embodied Robot for ASL Interpretation</a></h3>
      <p class="project-desc">
        A human-robot interaction study investigating how physical embodiment affects automated sign language interpretation. Pairs a Furhat social robot (dynamic gaze, facial expressions, synthesized speech) with a real-time OpenCV and MediaPipe 3D hand-tracking pipeline with temporal gesture filtering. A 26-participant within-subjects empirical study showed that physical embodiment significantly elevated user engagement (p &lt; .001) and sociability without compromising comprehension or trust.
      </p>
      <a class="project-link-btn" href="/project/asl-robot-interpreter/">Project Details &rarr;</a>
    </div>
  </div>

  <!-- Custom Gripper Card -->
  <div class="project-card">
    <img class="project-thumbnail" src="/img/tcps/TCPS_FingerMod.jpg" alt="Custom Sensorized Gripper Fingers" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">Mechatronics</span>
        <span class="tag-badge">FSR Sensors</span>
        <span class="tag-badge">CAD / 3D Print</span>
      </div>
      <h3 class="project-title">Custom Sensorized Gripper</h3>
      <p class="project-desc">
        Custom sensorized fingertips engineered for a Robotiq 2F-85 gripper on a UR3 arm, designed in Autodesk Fusion 360 and 3D printed. Houses a custom 5&times;3 force-sensitive resistor (FSR) array PCB with Arduino ADC acquisition to capture contact localization and grip force distribution during laparoscopic tool manipulation. Delivers real-time tactile telemetry back to operator haptic interfaces, preventing slippage and excessive clamping forces during teleoperated surgical tasks.
      </p>
      <a class="project-link-btn" href="/project/3d-prints/#modified-gripper-fingers-for-a-robot">View Details &rarr;</a>
    </div>
  </div>

  <!-- Adaptive IoT Data Management Card -->
  <div class="project-card">
    <img class="project-thumbnail" src="/img/project_tiles/portrait/AIOT.png" alt="Adaptive IoT Data Management" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">IoT Analytics</span>
        <span class="tag-badge">Time-Series</span>
        <span class="tag-badge">Edge ML</span>
        <span class="tag-badge">Aerospace</span>
      </div>
      <h3 class="project-title"><a href="/project/aiot/">Adaptive IoT Data Management</a></h3>
      <p class="project-desc">
        A Boeing-funded anomaly assessment and adaptive telemetry pipeline for aircraft cabin environmental control systems (ECS). Combines multi-zone MATLAB/Simulink physical simulations with supervised machine learning to classify sensor anomalies and assess severity across multivariate time series. Implements an error-bounded linear interpolation algorithm on the TICK stack, dynamically optimizing compression against reconstruction fidelity to achieve 96.6% storage savings.
      </p>
      <a class="project-link-btn" href="/project/aiot/">Project Details &rarr;</a>
    </div>
  </div>

  <!-- FPV Goggles Card
  <div class="project-card">
    <img class="project-thumbnail" src="/img/project_tiles/landscape/10_fpv.jpg" alt="FPV Goggles" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">Wearables</span>
        <span class="tag-badge">Low-Latency FPV</span>
        <span class="tag-badge">Medical</span>
      </div>
      <h3 class="project-title"><a href="/project/fpv-goggles/">FPV Goggles</a></h3>
      <p class="project-desc">
        Lightweight, ergonomic first-person-view glasses engineered for surgical training and remote observation with arthroscopic surgeons at IISc. Features a modular 3D-printed spectacle frame in Fusion 360 housing an Arduino Nicla Vision (STM32H7 dual-core ARM Cortex-M7/M4, 2MP camera). Streams low-latency wireless video over Wi-Fi without obstructing the surgeon's view, incorporating a spring-loaded lens tilt mechanism, integrated wire routing, and an ergonomic 10+ hour battery pack.
      </p>
      <a class="project-link-btn" href="/project/fpv-goggles/">Project Details &rarr;</a>
    </div>
  </div>
  -->

  <!-- BalanceBot Card -->
  <div class="project-card">
    <img class="project-thumbnail" src="/img/balancebot/sigi-robot.jpeg" alt="BalanceBot Robot" loading="lazy">
    <div class="project-body">
      <div class="project-tags">
        <span class="tag-badge">Control Systems</span>
        <span class="tag-badge">Simulink</span>
        <span class="tag-badge">Raspberry Pi</span>
      </div>
      <h3 class="project-title"><a href="/project/balancebot/">BalanceBot</a></h3>
      <p class="project-desc">
        A dynamic modeling and embedded control deployment pipeline for the Sigi two-wheeled inverted pendulum robot. Derived nonlinear 1-DOF and 2-DOF equations of motion in MATLAB/Simulink using Lagrangian mechanics, identified motor constants, and resolved encoder overflow. Designed and benchmarked PID, Phase-Lead, and LQR controllers, deploying C code to an onboard Raspberry Pi 3B+ via Simulink External Mode over I2C to evaluate sim-to-real transfer, actuator saturation, and gearbox backlash.
      </p>
      <a class="project-link-btn" href="https://github.com/nithishkgnani/BalanceBot">Code &rarr;</a>
      <a class="project-link-btn" href="/project/balancebot/">Project Details &rarr;</a>
    </div>
  </div>

</div>

<p style="text-align: right; margin-top: 10px;">
  <a href="/projects/" style="font-weight: 600;">View archive of all projects &rarr;</a>
</p>

---

<h2 id="publications">Publications</h2>

<div class="publication-item">
  <div class="pub-title">Utilizing Operator Intent for Haptic Teleoperation under high latencies</div>
  <div class="pub-authors">H.J.C. Kroep, P. Makridis, J. Huidobro, K. Wosten, D. Choudhary, <b>N. Gnani</b>, T.V. Prabhakar, S. Coppens, R.R. Venkatesha Prasad, K. Van Berlo</div>
  <div class="pub-venue">Accepted at IEEE Transactions on Mobile Computing (TMC)</div>
  <div class="pub-badges">
    <a class="badge-btn" href="https://ieeexplore.ieee.org/document/11091592" target="_blank" rel="noopener">IEEE Xplore</a>
    <a class="badge-btn" href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=11091592" target="_blank" rel="noopener">PDF</a>
    <span class="tag-badge">IEEE Journal</span>
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">RoboTwin: A Robotic Teleoperation Framework Using Digital Twins</div>
  <div class="pub-authors">Harsha Yelchuri, Diwakar Singh, <b>Nithish K Gnani</b>, T V Prabhakar, Chandramani Singh</div>
  <div class="pub-venue">Preprint (Under Review)</div>
  <div class="pub-badges">
    <a class="badge-btn" href="https://arxiv.org/abs/2506.01027" target="_blank" rel="noopener">arXiv Preprint</a>
    <a class="badge-btn" href="https://arxiv.org/pdf/2506.01027" target="_blank" rel="noopener">PDF</a>
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">EdgeP4: In-Network Edge Intelligence for a Tactile Cyber-Physical System Testbed Across Cities</div>
  <div class="pub-authors"><b>Nithish K Gnani</b>, Joydeep Pal, Deepak Choudhary, Himanshu V, Soumya R, Kaushal M, T V Prabhakar, Chandramani Singh</div>
  <div class="pub-venue">The 11th International Workshop on Computer and Networking Experimental Research using Testbeds (CNERT), IEEE INFOCOM 2024</div>
  <div class="pub-badges">
    <span class="badge-award">&#127942; Best Paper Award</span>
    <a class="badge-btn" href="https://doi.org/10.1109/INFOCOMWKSHPS61880.2024.10620719" target="_blank" rel="noopener">Paper</a>
    <a class="badge-btn" href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10620719" target="_blank" rel="noopener">PDF</a>
    <a class="badge-btn" href="https://github.com/nithishkgnani/EdgeP4" target="_blank" rel="noopener">Code</a>
    <a class="badge-btn" href="/img/other_images/CNERT24-Best-Paper.pdf" target="_blank" rel="noopener">Award Certificate</a>
    <span class="tag-badge">IEEE INFOCOM</span>
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">Towards a TSN-DetNet Intercity Testbed for Tactile Cyber-Physical Systems</div>
  <div class="pub-authors">Joydeep Pal, Deepak Choudhary*, <b>Nithish K Gnani*</b>, Chandramani Singh, T V Prabhakar, Hari Krishna A, A Paventhan (*Equal contributors)</div>
  <div class="pub-venue">The 11th International Workshop on Computer and Networking Experimental Research using Testbeds (CNERT), IEEE INFOCOM 2024</div>
  <div class="pub-badges">
    <a class="badge-btn" href="https://doi.org/10.1109/INFOCOMWKSHPS61880.2024.10620882" target="_blank" rel="noopener">Paper</a>
    <a class="badge-btn" href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10620882" target="_blank" rel="noopener">PDF</a>
    <span class="tag-badge">IEEE INFOCOM</span>
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">&mu;TAS: Design and implementation of Time Aware Shaper on SmartNICs to achieve bounded latency</div>
  <div class="pub-authors">Joydeep Pal, Deepak Choudhary, <b>Nithish K Gnani</b>, Chandramani Singh, T V Prabhakar</div>
  <div class="pub-venue">Preprint (Under Review)</div>
  <div class="pub-badges">
    <a class="badge-btn" href="https://arxiv.org/abs/2310.07480" target="_blank" rel="noopener">arXiv Preprint</a>
    <a class="badge-btn" href="https://arxiv.org/pdf/2310.07480.pdf" target="_blank" rel="noopener">PDF</a>
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">Sensor Identification via Acoustic Physically Unclonable Function</div>
  <div class="pub-authors">Girish Vaidya, T V Prabhakar, <b>Nithish K Gnani</b>, Ryan Shah, Shishir Nagaraja</div>
  <div class="pub-venue">Digital Threats: Research and Practice, 2022</div>
  <div class="pub-badges">
    <a class="badge-btn" href="https://doi.org/10.1145/3488306" target="_blank" rel="noopener">ACM Digital Library</a>
    <a class="badge-btn" href="https://dl.acm.org/doi/pdf/10.1145/3488306" target="_blank" rel="noopener">PDF</a>
    <span class="tag-badge">ACM Journal</span>
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">Judicious data management for sustaining an energy harvesting sensor node</div>
  <div class="pub-authors">Kaumudi Singh, Pratyush Shukla, Sachin S. M., <b>Nithish K Gnani</b>, T V Prabhakar, Joy Kuri</div>
  <div class="pub-venue">Concurrency and Computation: Practice and Experience, 2020</div>
  <div class="pub-badges">
    <a class="badge-btn" href="https://doi.org/10.1002/cpe.5997" target="_blank" rel="noopener">Wiley Online Library</a>
    <a class="badge-btn" href="https://onlinelibrary.wiley.com/share/author/K6MPERHBFRIRH9HTMIAC?target=10.1002/cpe.5997" target="_blank" rel="noopener">PDF</a>
    <span class="tag-badge">Wiley Journal</span>
  </div>
</div>

<p style="text-align: right; margin-top: 10px;">
  <a href="/teaching-and-talks/" style="font-weight: 600;">Teaching, Talks &amp; Demos &rarr;</a>
</p>

---

<h2>Education</h2>

<ul>
  <li>
    <strong>Master of Science in Autonomous Systems and Intelligent Robots</strong> &mdash; EIT Digital Master School (2026)
    <ul>
      <li>KTH Royal Institute of Technology, Sweden</li>
      <li>Polytech Nice Sophia, Université Côte d'Azur, France</li>
    </ul>
  </li>
  <li>
    <strong>Bachelor of Technology in Mechanical Engineering</strong> &mdash; National Institute of Technology Karnataka (NITK), India (2017)
  </li>
</ul>

---

<h2>Experience</h2>

<ul>
  <li>
    <strong>Master's Thesis &amp; Summer Worker, Vehicle Data and Driver Support</strong> &mdash; Scania (TRATON Group), Sweden (2026)
  </li>
  <li>
    <strong>Technical Associate &amp; Researcher</strong> &mdash; Indian Institute of Science (IISc), Bangalore (2019&ndash;2024)
    <ul>
      <li>Centre for Networked Intelligence (CNI) &bull; 2022&ndash;2024</li>
      <li>Research Associate, Dept. of Electronic Systems Engineering (DESE) &bull; 2021&ndash;2024</li>
      <li>Research Assistant, DESE &bull; 2019&ndash;2021</li>
    </ul>
  </li>
  <li>
    <strong>Team Leader, Maintenance</strong> &mdash; Hindustan Coca-Cola Beverages Pvt. Ltd. (2017&ndash;2018)
  </li>
</ul>

---

<h2>Awards &amp; Achievements</h2>

<ul>
  <li>
    <strong>Best Paper Award &ndash; CNERT 2024</strong> &mdash; IEEE INFOCOM
  </li>
  <li>
    <strong>First Place &ndash; 5G Hackathon 2020</strong> &mdash; Government of India (Team 5G-AMMAZING, $7,200 award)
  </li>
</ul>
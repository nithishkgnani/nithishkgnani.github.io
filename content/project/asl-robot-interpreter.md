---
title: "Embodied Robot and Textual Interfaces for Sign Language Interpretation"
date: 2025-12-11
author: "Nithish K Gnani"
tags: [social robotics, human-robot interaction, accessibility, Robotics]
categories: [Robotics, Accessibility]
draft: false
---
---
Location: KTH Royal Institute of Technology, Stockholm, Sweden  
Duration: Autumn 2025  
For: MSc Social Robotics course project   

---

{{< figure src="/img/social-robotics/user-study-setup.jpg" caption="User study setup with the Furhat robot, ASL video display, participant position and camera input." >}}

# Objective

To study how physical embodiment changes the way people experience automated sign language interpretation. We compared two ways of presenting the same interpreted content:

1. A standard text display.
2. A Furhat social robot that speaks the interpretation and uses gaze and head movement.

The project focused on the output modality of interpretation rather than building a new sign language recognition model. This allowed us to isolate whether embodiment, speech and social cues make the system feel more engaging, natural, trustworthy or partner-like.

# System Design

We built two paired subsystems, each with a robot version and a display version. The underlying logic was kept equivalent across modalities so that only the output channel changed.

{{< mermaid >}}
flowchart LR
    participant[Participant] --> task{Task}
    task --> rps[Rock-Paper-Scissors]
    task --> asl[ASL interpretation]
    rps --> vision[Webcam + MediaPipe gesture detection]
    asl --> videos[ASL videos + translations]
    vision --> output{Output modality}
    videos --> output
    output --> robot[Robot: speech, gaze, head movement]
    output --> display[Display: text interface]
    robot --> study[User study ratings]
    display --> study

    classDef actor fill:#e0f2fe,stroke:#0369a1,color:#0f172a,stroke-width:1.5px
    classDef task fill:#fef3c7,stroke:#b45309,color:#0f172a,stroke-width:1.5px
    classDef processing fill:#ecfdf5,stroke:#047857,color:#0f172a,stroke-width:1.5px
    classDef outputNode fill:#fce7f3,stroke:#be185d,color:#0f172a,stroke-width:1.5px
    classDef result fill:#ede9fe,stroke:#6d28d9,color:#0f172a,stroke-width:1.5px

    class participant actor
    class task,rps,asl task
    class vision,videos processing
    class output,robot,display outputNode
    class study result
{{< /mermaid >}}

## Gesture-based Rock-Paper-Scissors

The active interaction task was a Rock-Paper-Scissors game using a webcam and MediaPipe Hands. The camera pipeline extracted hand landmarks and classified gestures using deterministic finger-extension rules for rock, paper and scissors. A stability filter accepted a gesture only after consistent detections, reducing false triggers during real-time play.

In the robot condition, the Furhat robot greeted the participant, ran the game loop through speech, announced its move and reacted to the result. In the display condition, the same game state, prompts and results were shown through a fullscreen graphical interface.

## ASL Interpretation Interface

The interpretation task used a Wizard-of-Oz style setup with prerecorded ASL videos and fixed English translations. No autonomous ASL recognition was used in this study. Instead, the videos and translations were controlled so that both modalities presented the same information.

In the Furhat condition, the robot turned toward the ASL video, waited while the signer was shown, turned back to the participant and spoke the translated sentence. In the text condition, the translation was shown as large centered text after the same video sequence.

# User Study

We ran a within-subjects study with 26 participants. Each participant experienced both the robot and display conditions for the Rock-Paper-Scissors task and the ASL interpretation task. The order of modalities was counterbalanced.

Participants rated engagement, social presence, naturalness, trust and comprehension. We also collected comparative preferences and open-ended feedback after the tasks.

# Results

## Active Interaction

The robot made the game feel more engaging without changing the perceived quality of gesture recognition. Participants rated the robot higher for fun, attention, liveliness and naturalness, while competence and gesture-detection accuracy remained comparable to the display.

{{< figure src="/img/social-robotics/result-rps-ratings.png" caption="User ratings for the Rock-Paper-Scissors task." >}}

## ASL Interpretation

For ASL interpretation, the robot was perceived as more sociable, emotional and partner-like than the text display. However, perceived trust was the same for both systems, and comprehension was similar. This suggests that the robot added social presence without improving or reducing the perceived reliability of the interpreted content.

{{< figure src="/img/social-robotics/result-asl-ratings.png" caption="Social and functional ratings for the ASL interpretation task." >}}

## Preference

Participants strongly preferred the robot for interaction: 87.5% preferred it for Rock-Paper-Scissors and 75% preferred it for ASL interpretation. When asked specifically about trustworthiness, preferences were split, with the text display slightly preferred.

{{< figure src="/img/social-robotics/result-preferences.png" caption="Overall participant preferences between the robot and display interfaces." >}}

# Design Takeaways

The main finding was a clear split between functional trust and social preference. The Furhat robot did not make the interpretation more trusted than text, but it made the interaction feel more social and connected.

This suggests that embodied robot interpreters are useful in settings where social connection matters, such as education, service interactions or face-to-face assistance. For fast, high-stakes or purely administrative communication, a text display may still be more efficient.

The project also highlighted the importance of keeping a text fallback. Participants with more negative attitudes toward robots were less likely to prefer the robot in the active interaction task, so embodiment should be treated as a context-aware option rather than a universal replacement for text.

---

<div style="text-align: right">
<a href="/projects">Back to Projects</a>
</div>

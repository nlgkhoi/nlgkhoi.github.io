---
title: "Sound of Silence – Vietnamese Sign Language Translation Application"
excerpt: "A project aimed at empowering the hearing impaired through an AI-driven device that translates sign language into text and speech. Features a portable camera module and an efficient mobile application, achieving significant recognition accuracy and making an impactful contribution to the community.<br/><img src='/images/demo_sos.gif' style='width: 60%;'>"
collection: portfolio
---

PDF (in Vietnamese): [Download here](/files/SOS_paper.pdf)

## Solution Idea:

The "Sound of Silence" project aims to facilitate communication for people with hearing impairments through an innovative device that translates sign language into text and speech. This initiative is significant in Vietnam, where there is a substantial population with hearing difficulties but limited availability of sign language interpreters​​.

## Important System Components:

- **Camera Module**: A compact camera and electronic components are installed in a biodegradable plastic (Polylactic Acid - PLA) housing attached to a hat. This setup ensures a stable image input without much external disturbance and enhances portability​​.
- **Mobile Application**: The application uses AI and computer vision technologies to convert sign language gestures into text and speech, displayed on the smartphone screen and broadcast through speakers. It's designed for low hardware requirements, making it accessible to a broad range of mobile devices, including older models​​.

## Implementation:

- **AI Application**: The AI system transforms sign language gestures into text and speech. It uses Google's Mediapipe for feature extraction and a deep learning model for gesture recognition. Finally, Google's Text2Speech technology converts the text into speech​​.

<div style="text-align: center;">
    <img src="/images/port_2_pipeline.png" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 1: System Design</em>
</div>

- **Model Accuracy**: The gesture recognition model achieved an average accuracy of 89% in identifying hand gestures. However, the accuracy for recognizing hand positions and movements was around 60%​​.

## Results:

- **Portability and Efficiency**: The device stands out for its portability and efficient operation on mobile phones without the need for high-end hardware.
- **Community Impact**: The project has garnered attention, notably from the Vĩnh Long Television and Radio Station, which collaborated with Ho Chi Minh City University of Technology and team members to publicize the product​​.

<div style="text-align: center;">
    <img src="/images/demo_sos.gif" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 2: Prototype Demonstration</em>
</div>


In summary, the "Sound of Silence" project provides an innovative and practical solution to bridge communication gaps for the hearing impaired. With its portable design, efficient AI implementation, and community outreach, it represents a significant step towards inclusive communication technology.
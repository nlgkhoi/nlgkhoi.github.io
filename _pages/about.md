---
permalink: /
title: "👋 Hello there, I'm Khoi!"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<div style="display: flex; align-items: start; margin: 20px;">
    <div style="flex-grow: 1; padding-right: 40px; line-height: 1.6;">
        💼 AI Engineer @ System 2 AI, Finland — building compute infrastructure for continual-learning LLM agents on LUMI<br><br>
        ✍️ Method co-author on <em>Targeted-Edit Supervision</em>, submitted to NeurIPS 2026 (under review)<br><br>
        🧑‍🎓 Double-Degree MSc in Data Science @ Aalto University (Finland) and University of Twente (Netherlands), graduated with honours, 2025<br><br>
        🧑‍🎓 Bachelor in Computer Science @ Ho Chi Minh City University of Technology, Vietnam — Top-2 graduate of the 2019-2023 cohort<br><br>
        💼 Former AI Engineer @ Quy Nhon AI Research and Application Center (FPT Software), Vietnam<br><br>
        🦾 My interest lies in Large Language Models, continual learning, distributed training, and the engineering frontier of LLM systems<br><br>
        🎼 I write music in my free-time. My genres are Rap and R&B.<br><br>
        📖 "Embracing Kaizen mindset in every aspect of life"<br><br>
    </div>
    <div>
        <img src="/images/pf_img_2.png" alt="Illustration of the harmonic living of AI and human" style="width: 400px;">
    </div>
</div>

# 🍳 Skills

| **Programming Languages** | Python (Advanced), C++ (Intermediate) |
| **Frameworks**            | PyTorch (Advanced), Tensorflow, Flask, Django etc. |
| **Libraries**             | NumPy, Pandas, Matplotlib, Seaborn, OpenCV, Pillow, etc. |
| **Operating Systems**     | Linux (CLI), Windows, MacOS |
| **Cloud**                 | AWS EC2, AWS S3 |
| **Others**                | Shell script, Docker, RabbitMQ, Kafka, CI/CD pipeline |
| **Language proficiency**  | C1 English Level |

# 📌 Selected Projects
## Multi-Node LLM Training & Serving Infrastructure on LUMI @ System 2 AI, Finland
As compute-infrastructure lead at System 2 AI, I own the multi-node training and serving stack on the LUMI (CSC) supercomputer — SLURM / NCCL / FSDP + tensor parallelism for training, vLLM-based serving with a custom container that tracks the latest vLLM release and delivers a 2–3× speedup over stock images. Recent wins include bringing up Kimi K2.6 and Qwen3.5-397B on just two LUMI nodes; the 397B model sustains roughly 50% of a single-node Qwen3-32B's throughput while being ~12× larger.<br/>

Keywords: *llm, distributed training, fsdp, tensor parallelism, vllm, lumi, multi-node serving, continual learning*

## Targeted-Edit Supervision (NeurIPS 2026 submission, under review) @ System 2 AI, Finland
A new method for supervised knowledge editing in LLMs. I authored the method — designed and ran the first proof-of-concept experiment that seeded the technique later developed into the submitted paper — and implemented the training pipeline on top of S2's multi-node LUMI infrastructure.<br/>

Keywords: *knowledge editing, supervised fine-tuning, llm, continual learning*

## Optimizing the Computational Efficiency of Training and Inference for Large Language Models @ System 2 AI Oy, Finland (MSc Thesis)
Applying advanced 2D parallelism techniques, i.e., Tensor Parallelism (TP) - FSDP, to train Llama 3 and 3.1 family models on substentially longer sequence length on limited hardware capability.<br/>

<img src='/images/megatron-lm.png' style='width: 60%;'>

See more: [Here](/portfolio/portfolio-4/)

Keywords: *tensor parallelism, fsdp, megatron-lm, large language model, llama, machine learning*

## Table OCR pipeline with branching mechanism to handle different types of tabular documents (Capstone Project) @ HCMUT, Vietnam
An innovative approach to OCR of tables in documents, focusing on Table Detection and Structure Recognition, with the development of a robust Table Extraction Pipeline. Significant progress in Transformer-based model pruning enhances efficiency without compromising accuracy.<br/><img src='/images/port_1_outputs.png' style='width: 60%;'>

See more: [Here](/portfolio/portfolio-1/)

Keywords: *table detection, table structure recognition, OCR, computer vision, transformer-based model, machine learning*

## Vietnamese Sign Language Translation Application @ HCMUT, Vietnam
A project aimed at empowering the hearing impaired through an AI-driven device that translates sign language into text and speech. Features a portable camera module and an efficient mobile application, achieving significant recognition accuracy and making an impactful contribution to the community.<br/><img src='/images/demo_sos.gif' style='width: 60%;'>

See more: [Here](/portfolio/portfolio-2/)

Keywords: *sign language translation, transformer, computer vision, multi-modal modelling, mediapipe, IoT, machine learning, vietnamese*

## Watermark Removal via Autoencoder-Based Approach
Developing an autoencoder model to effectively remove watermarks from images, addressing a key challenge in real estate image sharing.<br/><img src='/images/port_3_ex1.jpg' style='width: 60%;'><br><img src='/images/port_3_ex2.jpg' style='width: 60%;'>

See more: [Here](/portfolio/portfolio-3/)

Keywords: *watermark removal, autoencoder, data augmentation, computer vision, machine learning*

# 👔 Professional Experience
## 🧪 AI Engineer
**System 2 AI**  
_Apr 2025 - Present, Helsinki, Finland_
- Compute-infrastructure lead for S2's continual-learning research stack on LUMI (CSC): multi-node LLM training (SLURM / NCCL / FSDP + tensor parallelism) and vLLM-based serving, supporting the five-person research team.
- Built a custom training/serving container that tracks the latest vLLM release, enabling same-day support for new model launches and delivering a 2–3× speedup in inference and training.
- Brought up large open-weights foundation models with aggressive multi-node serving — including Kimi K2.6 and Qwen3.5-397B at usable speed on just two LUMI nodes.
- Method co-author on *Targeted-Edit Supervision* (submitted to NeurIPS 2026, under review): designed and ran the first proof-of-concept experiment that seeded the technique developed into the submitted paper.

## 🤖 Artificial Intelligence Engineer
**Quy Nhon AI Research and Application Center (FPT Software Quy Nhon)**  
_Nov 2021 - Jun 2023, Quy Nhon, Vietnam_
- Developed core models for the akaOCR AI platform.
- Collected and pre-processed training text data.
- Integrated deep learning models into various outsourcing projects including Japanese Financial Statement Analysis, Table Reconstruction

## 🧑‍💻 Artificial Intelligence Engineer (Apprenticeship)
**Rever Real Estate Technology Co. Ltd**  
_Nov 2020 - Nov 2022, Ho Chi Minh City, Vietnam_
- Specialized in researching and proposing CV solutions including watermark removal, contract auto-filling, and existing scene detection
- Implemented and tested deep learning models.
- Dockerized and implemented RESTful APIs.

# Recommendations
## 🎓 Assoc. Prof. Quan Thanh Tho
_Vice Dean, Faculty of Computer Science and Engineering, HCMUT_  
_Email: [qttho@hcmut.edu.vn](mailto:qttho@hcmut.edu.vn)_  
_LinkedIn: [LinkedIn Profile](https://www.linkedin.com/in/qttho/)_
> "Assoc. Prof. Quan Thanh Tho, a distinguished faculty member at HCMUT, is well-versed in formal methods, program analysis/verification, the Semantic Web, machine learning/data mining, and intelligent systems. His academic journey spans a B.Eng. in Information Technology from HCMUT and a Ph.D. from Nanyang Technological University, Singapore."  
> **– Assoc. Prof. Quan Thanh Tho**

## 💼 Dr. Nguyen Chi Hoang
_AI R&D Team Leader, FPT Software Da Nang_  
_Email: [hoangnc3@fsoft.com.vn](mailto:hoangnc3@fsoft.com.vn)_  
_LinkedIn: [LinkedIn Profile](https://www.linkedin.com/in/hoang-nguyen-chi-b31860123/)_
> "With a rich background in Information Technology and a Ph.D. from Claude Bernard University Lyon 1, France, Dr. Nguyen Chi Hoang leads AI R&D at FPT Software Da Nang. His expertise has contributed to over 20 projects globally, focusing on AI adoption strategies, including developing predictive applications and software for stock price forecasting."  
> **– Dr. Nguyen Chi Hoang**

## 🌟 Mr. Vu Hong Chien
_Director, Quy Nhon AI Research and Application Center, FPT Software Quy Nhon_  
_Email: [chienvh1@fsoft.com.vn](mailto:chienvh1@fsoft.com.vn)_  
_LinkedIn: [LinkedIn Profile](https://www.linkedin.com/in/chienvh1/)_
> "Mr. Vu Hong Chien, a recognized leader in technology, was named FPT Under 35 in 2017. His career at FPT Software includes roles as Head of the FQC Department and CTO of FPT DPS, leading up to his current position as the Director of Quy Nhon AI Research and Application Center."  
> **– Mr. Vu Hong Chien**

# 🎙️ Talks and Community Contributions

## 📕 Google Developer Student Club - How-to-AI Series
_Technical Speaker & Academic Team Leader_  
_Oct 2022 - Dec 2022_
- Developed and presented content for a five-day series on Artificial Intelligence and career paths in the AI field.
- Collaborated with AI experts to organize fireside chats for HCMUT students, fostering a deeper understanding of AI technologies and career opportunities.

<div style="text-align: center;">
    <img src="/images/talk_1_img_1.png" alt="A moment from the webinar" style="width: 80%;">
    <br>
    <img src="/images/talk_1_img_2.png" alt="A moment from the webinar" style="width: 80%;">
    <br>
    <img src="/images/talk_1_img_3.JPG" alt="A moment from the webinar" style="width: 80%;">
    <br>
    <em>Moments from the webinar</em>
</div>

## 📗 Google Developer Student Club - Machine Learning Workshop
_Technical Speaker & Academic Team Leader_  
_Feb 2022 - Mar 2022_
- Conducted sessions on fundamental concepts and simple algorithms in Machine Learning for HCMUT students.
- Partnered with CoderSchool to provide advanced insights into Deep Learning, enhancing the technical knowledge of attendees.

<div style="text-align: center;">
    <img src="/images/talk_2_img_1.jpg" alt="A moment from the workshop" style="width: 80%;">
    <br>
    <img src="/images/talk_2_img_2.jpg" alt="A moment from the workshop" style="width: 80%;">
    <br>
    <img src="/images/talk_2_img_3.jpg" alt="A moment from the workshop" style="width: 80%;">
    <br>
    <em>Moments from the workshop</em>
</div>

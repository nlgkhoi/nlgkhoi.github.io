---
title: "Watermark Removal via Autoencoder-Based Approach"
excerpt: "Developing an autoencoder model to effectively remove watermarks from images, addressing a key challenge in real estate image sharing.<br/><img src='/images/port_3_ex1.jpg' style='width: 60%;'><br><img src='/images/port_3_ex2.jpg' style='width: 60%;'>"
collection: portfolio
---

## Introduction and Motivation:

In the Vietnamese real estate sector, the exchange of property images among brokerage firms is commonplace. A recurrent issue arises when images shared retain watermarks, and due to certain constraints, obtaining watermark-free versions is not feasible. This scenario necessitates a robust technological solution capable of eradicating watermarks from images. The primary challenge lies in the diverse characteristics of these watermarks, which vary in brightness, opacity, size, rotation, and resolution, including some previously unseen versions. This complexity demands an innovative approach, as a predefined watermark dataset is unavailable.

## Technical Approach and Implementation:

- **Data Augmentation Technique**: Given the limited availability of training data, a bespoke data augmentation algorithm was developed. This algorithm artificially adds watermarks to random images, mimicking a range of variations in brightness, opacity, size, rotation, and resolution, thereby creating a realistic dataset representative of actual watermarked images.

- **Autoencoder Architecture**: An advanced autoencoder model was engineered and trained on this artificially generated dataset. The objective was to enable the model to produce images devoid of watermarks, effectively `'learning'` to eliminate the watermark characteristics from the input images.

<div style="text-align: center;">
    <img src="/images/port_3_pipeline.jpeg" alt="Autoencoder Architecture" style="width: 90%;">
    <br>
    <em>Figure 1: Autoencoder Architecture</em>
</div>

## Observations and Results:

- The autoencoder displayed commendable efficacy on images where the watermarks were fully known beforehand. This includes instances where transparent versions of the watermarks were utilized in the training phase. However, the model demonstrated limitations in dealing with unseen watermarks or those for which masks were not readily available.

## Future Enhancement Directions:

- **Data Augmentation Expansion**: The current augmentation methodology could benefit from the incorporation of advanced generative models, such as Generative Adversarial Networks (GANs), to create indistinguishable watermarked images that closely resemble real-life scenarios.

- **Autoencoder Evolution**: Exploring alternative architectures like Variational Autoencoders (VAEs) or other generative models could potentially enhance the watermark removal capabilities, offering more robust solutions to varying watermark challenges.

<div style="text-align: center;">
    <img src="/images/port_3_ex1.jpg" alt="Watermark Removal Example 1" style="width: 90%;">
    <br>
    <img src="/images/port_3_ex2.jpg" alt="Watermark Removal Example 2" style="width: 90%;">
    <br>
    <img src="/images/port_3_ex3.jpg" alt="Watermark Removal Example 3" style="width: 90%;">
    <br>
    <em>Figure 2: Results of watermark removal</em>
</div>

## Summary:
The watermark removal project represents a significant stride in addressing a specific challenge in the real estate domain. By leveraging an autoencoder-based approach, complemented by a custom data augmentation technique, the project showcases promising results in removing known watermarks. However, the model's current limitations in handling unseen watermarks highlight the need for further research and development in this area. Future enhancements, involving more sophisticated generative models and autoencoder variations, hold the potential to refine this solution, making it more versatile and effective in diverse real-world scenarios.

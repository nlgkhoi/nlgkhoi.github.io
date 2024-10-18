---
title: "Optimizing the computational efficiency of LLM training and inference through advanced parallelism techniques."
excerpt: "Applying advanced 2D parallelism techniques, i.e., Tensor Parallelism (TP) - FSDP, to train Llama 3 and 3.1 family models on substentially longer sequence length on limited hardware capability<br/><img src='/images/megatron-lm.png' style='width: 60%;'><br>See more: <a href='/portfolio/portfolio-1/'>Here</a><br>Keywords: <em>tensor parallelism, fsdp, megatron-lm, large language model, llama, machine learning</em>"
collection: portfolio
---

PDF: [Download here](/files/Final_Thesis_Huan_Khoi.pdf)

Keywords: *tensor parallelism, fsdp, megatron-lm, large language model, llama, machine learning*

**"Optimizing the computational efficiency of LLM training and inference through advanced parallelism techniques."**, supervised by Prof. Alexander Ilin Ph.D. and Dr. Harri Vapola, conducted at System 2 AI Oy. The project aims to apply advanced parallelism techniques, e.g., Fully Sharded Data Parallel (FSDP), Tensor Parallel (TP), etc. to the training of Large Language Models (LLM), specifically Llama 3 model family.

The core problems tackled include the implementation of tensor parallelism technique introduced in [Megatron-LM](https://arxiv.org/abs/1909.08053) paper

<div style="text-align: center;">
    <img src="/images/megatron-lm.png" alt="Megatron-LM" style="width: 90%;">
    <br>
    <em>Figure 1: Table Extraction Tasks Survey</em>
</div>

<div style="text-align: center;">
    <img src="/images/port_1_pipeline.jpg" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 2: Table OCR pipeline</em>
</div>

Experimental evaluations of various Table Detection (TD) and Table Structure Recognition (TSR) models were conducted, utilizing both public and private datasets. These datasets included manually labeled financial statements, receipts, and inventory management tables, among others. Evaluation metrics such as recall, precision, F1-score across different Intersection over Union (IoU) thresholds, and [GriTS](https://arxiv.org/abs/2203.12555) were used.

Key findings from these experiments include:
- CDeCNet achieved the highest precision and F1-score at all thresholds.
- DETR and CascadeTabNet also showed high precision, while Cascade Mask RCNN trained on TNCR displayed the highest recall.
- Notably, no single model completely outperformed the others.

The CDeCNet model, despite its high precision, had a significantly larger number of parameters, leading to slower inference times. In contrast, the DETR model, based on a Transformer architecture, had the smallest number of parameters and was efficient in accommodating variable numbers of objects.

A standout achievement of this project was the development of a pruning method for Transformer-based models. This method outperformed traditional uniform pruning techniques, reducing the model's parameters up to 66% while only experiencing a minimal drop in performance (2% - 4.3% in AP and AR; 1% in GriTS_Top).

## Experimental Result

<div style="text-align: center;">
    <img src="/images/TSR_results.png" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 3: Pruned TSR Model Experimental Results</em>
</div>

<div style="text-align: center;">
    <img src="/images/TD_results.png" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 4: Pruned TD Model Experimental Results</em>
</div>

<div style="text-align: center;">
    <img src="/images/Speedup.png" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 5: Model Speedup Measurement</em>
</div>

Overall, the project successfully built a modular, lightweight pipeline for various table types and domains, significantly advancing the field of table OCR. It laid the groundwork for future research, particularly in improving pre- and post-processing methods and further developing pruning techniques for Transformer-based models.

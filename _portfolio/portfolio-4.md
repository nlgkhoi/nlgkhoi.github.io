---
title: "Optimizing the computational efficiency of LLM training and inference through advanced parallelism techniques."
excerpt: "Applying advanced 2D parallelism techniques, i.e., Tensor Parallelism (TP) - FSDP, to train Llama 3 and 3.1 family models on substentially longer sequence length on limited hardware capability<br/><img src='/images/megatron-lm.png' style='width: 60%;'><br>See more: <a href='/portfolio/portfolio-1/'>Here</a><br>Keywords: <em>tensor parallelism, fsdp, megatron-lm, large language model, llama, machine learning</em>"
collection: portfolio
---

<!-- PDF: [Download here](/files/Final_Thesis_Huan_Khoi.pdf) -->

Keywords: *tensor parallelism, fsdp, megatron-lm, large language model, llama, machine learning*

**"Optimizing the computational efficiency of LLM training and inference through advanced parallelism techniques."**, supervised by Prof. Alexander Ilin Ph.D. and Dr. Harri Vapola, conducted at System 2 AI Oy. The project aims to apply advanced parallelism techniques, e.g., Fully Sharded Data Parallel (FSDP), Tensor Parallel (TP), etc. to the training of Large Language Models (LLM), specifically Llama 3 model family.

The core problems tackled include the implementation of tensor parallelism technique, introduced in [Megatron-LM](https://arxiv.org/abs/1909.08053) paper, using native Pytorch tensor parallel support, instead of relying on external library, e.g., `accelerate` by Huggingface. Another key implementation include the combination of FSDP and TP to combinatorially leverage the advantages of both methods. 

<div style="text-align: center;">
    <img src="/images/megatron-lm.png" alt="Tensor Parallel Paradigm in main Transformer components" style="width: 90%;">
    <br>
    <em>Figure 1: Tensor Parallel paradigm in main Transformer components</em>
</div>

Key verification steps included:
- Verify the correct distribution of tensor weights across GPUs (devices). This step requires a careful inspection of weights shape and values.
- Verify the local outputs of all components as well as the final logits are correctly computed as in the original, non-parallel model.
- Verify the correct gradient updates of all parameters, accounting for the lost of precision due to the use of bfloat16 data type.

Key findings from these experiments include:
- The adaptation of TP into Transformer-based models often require changing the implementation code of the core model; however, the changes are intuitive and interpretable.
- DTensor is a special Pytorch data type and has confused interface when exposed to call. This requires the understanding of the abstract distributed graph behind when doing debugging.
- Underlying distributed tensors stored in local DTensors have to be handled with care and total understanding when it comes to modification of their content.
- APIs for loading and saving distributed TP model weights are not yet provided by Pytorch and has to be manually implemented.
- FSDP can be applied on top of TP for sufficient and effective distribution of tensor weights across multiple nodes.
- Good practice: Apply FSDP for inter-node distribution and TP for intra-node distribution.
- FSDP CPU-offloading capability is the key for multi-node scale-up training to overcome theoretical GPU memory capability, enabling to train LLMs as long as they can be fitted on the total amount of memory.
- Together with gradient checkpointing and CPU-offloading, FSDP-TP 2D parallelism enables significant long sequence training and scaling-up by factor of GPUs as well as easy scaling training just by adding more nodes. 

A standout achievement of this project was the successfuly implementation of the 2D parallelism technique FSDP-TP to the multi-node training of Llama 3 models on the Puhti supercomputer, allowing for a scale-up in training sequence length by a factor of the GPUs. Specifically, we manage to train a Llama 3 70B model on two GPU nodes, each of which has 4 32GB GPU, with the total of 256 GB of memory. The maximum sequence length is approximately 5200 tokens which is almost 2 times longer compared to when only FSDP is applied, in this settings of 4 GPUs per node.

## Methods for verifying the correct inference/training computation:

<div style="text-align: center;">
    <img src="/images/images/top_k_mae.png" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 2: Token matching percentages and MAE of the output logits of the TP applied model and non-parallel model</em>
</div>
The high token matching percentages as well as low MAE of output logits in different top-k values shows that the sacrificing of precision is acceptable and does not affect the inference output of the model.

<div style="text-align: center;">
    <img src="/images/Comparision of Training loss.png" alt="Alternative Text" style="width: 90%;">
    <br>
    <em>Figure 3: Training Loss trajectories of different models applied different parallelism techniques as well as the non-parallel model</em>
</div>
It can be seen that the training loss trajectories are all the same across different parallelism settings, implying the correct implementation of the parallelism techniques.

Overall, the project successfully implemented the 2D-parallelism techinques, i.e., FSDP-TP, to the training of Llama 3 model family and methods for efficient model weights loading and saving. This enable the infinite scaling of sequence length and batch size just simply by adding more nodes.

# Sustainability_Attacks_on_AI

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

There are thousands of publications on making AI more energy and time efficient. We subsume these proposals as sustainability measures for now.

From an AI security perspective: Can a bad actor nullify these optimizations for fun (and profit)? We call this an **energy-latency attack**. This is a novel angle on AI security which will become very relevant very soon. [Sponge Examples: Energy-Latency Attacks on Neural Networks](https://ieeexplore.ieee.org/abstract/document/9581273) will give you a good idea on energy-latency attacks.

The objective of this repo is to match sustainability measures to existing attacks. This way, we can identify trends and possibly blank spots.

<!-- Find out how AI is being made more sustainable - and how malicious actors can make it less so. -->

For now, this is a collection of papers and articles with personal annotations. It can already help you find sources on (the robustness of) sustainable AI.

Feel free to star and fork. Contact me if you are curious (See my Github bio).

# Contents
- [Motivation](#Motivation)
- [Sustainability](#Sustainability)
- [Attacks](#Attacks)

# Motivation
| Publication                                                                                                                                  | Notes                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [A New Golden Age in Computer Architecture: Empowering the Machine-Learning Revolution](https://ieeexplore.ieee.org/document/8259424)  | Journal article about the rise of AI hardware                                                                                                                                                  |
| [Energy and Policy Considerations for Deep Learning in NLP](https://aclanthology.org/P19-1355/)                                        | "LLM-Training consumes 5 Car lifetime CO2e Emissions”                                                                                                                                          |
| [Carbon Emissions and Large Neural Network Training](https://arxiv.org/abs/2104.10350)                                                 | "GPT-3 training consumed as much CO2e as 5 rountrips between San Francisco and New York"                                                                                                       |
  | [Characterizing Sources of Ineffectual Computations in Deep Learning Networks](https://ieeexplore.ieee.org/document/8573509)           | Gives us some clues which acceleration options have the biggest influence on reducing work. See Fig.1 in the paper for ranking.                                                                |
| [Deep Learning's Diminishing Returns: The Cost of Improvement is Becoming Unsustainable](https://ieeexplore.ieee.org/document/9563954) | "We will achieve 95% ImageNet accuracy by 2025, but it will cost as many CO2 emission as New York City consumes in a month"                                                                    |
| [The computational limits of deep learning](https://arxiv.org/abs/2007.05558)                                                          | Same authors as [Deep Learning's Diminishing Returns: The Cost of Improvement is Becoming Unsustainable](https://ieeexplore.ieee.org/document/9563954)                                         |
| [The Carbon Footprint of Machine Learning Training Will Plateau, Then Shrink](https://ieeexplore.ieee.org/document/9810097)            | Disputes [Deep Learning's Diminishing Returns: The Cost of Improvement is Becoming Unsustainable](https://ieeexplore.ieee.org/document/9563954), as sustainability measures will increase too. |
| [Sustainable AI: Environmental Implications, Challenges and Opportunities](https://arxiv.org/abs/2111.00364)                           | Facebook AI reports trillions of inferences across datacenters                                                                                                                                 |
| [Tensor Dash presentation video](https://www.youtube.com/watch?v=hMH-cp-EY3Q)                                                          | Has some nice charts on rising energy consumption of DNNs at the beginning                                                                                                                     |
| [The Carbon Footprint of Transformers](https://www.youtube.com/watch?v=ftWlj4FBHTg)                                                    |                                                                                                                                                                                                |
| Huggingface models lists carbon emitted                                                                                                | see [distilgpt2](https://huggingface.co/distilgpt2), it uses [https://mlco2.github.io/impact/#compute](https://mlco2.github.io/impact/#compute)                                                |

# Sustainability
## Sparsity
### General Sparsity (TODO: sort later)
| Publication                                                                                                                                        | Venue/Journal/Journal | Notes                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------|
| [Minimizing Energy Consumption of Deep Learning Models by Energy-Aware Training](https://arxiv.org/pdf/2307.00368.pdf)                             |||
| [Automatic Generation of Multi-Precision Multi-Arithmetic CNN Accelerators for FPGAs](https://ieeexplore.ieee.org/document/8977872)                |||
| [Accelerating Sparse Deep Neural Networks](https://arxiv.org/abs/2104.08378)                                                                       |                       | NVIDEA 2:4 structured sparsity in Ampere Architecture |
  | [Sparseloop: An Analytical Approach To Sparse Tensor Accelerator Modeling](https://ieeexplore.ieee.org/document/9923807)                           |||
  | [Harnessing Manycore Processors with Distributed Memory for Accelerated Training of Sparse and Recurrent Models](https://arxiv.org/abs/2311.04386) |||
  | [Sparse-DySta: Sparsity-Aware Dynamic and Static Scheduling for Sparse Multi-DNN Workloads](https://dl.acm.org/doi/abs/10.1145/3613424.3614263)    |||
  | [Pruning and Quantization for Deep Neural Network Acceleration: A Survey](https://arxiv.org/abs/2101.09671)                                                                                                                                                   |||

### Activation Sparsity Accelerators
| Publication                                                                                                                                                                                                                                    | Venue/Journal/Journal                                         | Notes                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------|:--------------------------------------------------|
| [EIE: Efficient Inference Engine on Compressed Deep Neural Network](https://dl.acm.org/doi/10.1145/3007787.3001163)                                                                                                                            | 2016 ACM SIGARCH Computer Architecture News                   | Fundamental paper for hardware-based acceleration |
  | [Retrospective: EIE: Efficient Inference Engine on Sparse and Compressed Neural Network](https://arxiv.org/abs/2306.09552)                                                                                                                     |                                                               |                                                   |
| [Inducing and Exploiting Activation Sparsity for Fast Neural Network Inference](https://proceedings.mlr.press/v119/kurtz20a.html)                                                                                                              | PMLR 2020                                                     |                                                   |
| [Accelerating convolutional neural networks via activation map compression](https://ieeexplore.ieee.org/document/8953659)                                                                                                                      | 2019 IEEE/CVF                                                 |                                                   |
| [Compressing DMA Engine: Leveraging Activation Sparsity for Training Deep Neural Networks](https://ieeexplore.ieee.org/document/8327000)                                                                                                       | 2018 IEEE Symposium on High-Performance Computer Architecture |                                                   |
| [SNICIT: Accelerating Sparse Neural Network Inference via Compression at Inference Time on GPU](https://dl.acm.org/doi/abs/10.1145/3605573.3605625)                                                                                            | ICPP 2023                                                     |                                                   |
| [TensorDash: Exploiting Sparsity to Accelerate Deep Neural Network Training](https://ieeexplore.ieee.org/document/9251995)                                                                                                                     |                                                               |                                                   |
| [Accelerating Deep Neural Networks via Semi-Structured Activation Sparsity](https://openaccess.thecvf.com/content/ICCV2023W/RCV/html/Grimaldi_Accelerating_Deep_Neural_Networks_via_Semi-Structured_Activation_Sparsity_ICCVW_2023_paper.html) | ICCV Workshop 2023                                            |                                                   |
| [Two sparsities are better than one: unlocking the performance benefits of sparse–sparse networks](https://iopscience.iop.org/article/10.1088/2634-4386/ac7c8a/meta#nceac7c8abib69)                                                            |                                                               |                                                   |
| [Exploiting Activation Sparsity for Fast CNN Inference on Mobile GPUs](https://arxiv.org/pdf/2309.06626.pdf)                                                                                                                                   | ACM Transactions on Embedded Computing Systems 2021           |                                                   |
| [DASNet: Dynamic Activation Sparsity for Neural Network Efficiency Improvement](https://ieeexplore.ieee.org/document/8995451)                                                                                                                  | ICTAI 2019                                                    |                                                   |
  | [A novel zero weight/activation-aware hardware architecture of convolutional neural network](https://dl.acm.org/doi/10.5555/3130379.3130723)                                                                                                   |                                                               |                                                   |
  | [SCNN: An Accelerator for Compressed-Sparse Convolutional Neural Networks](https://arxiv.org/abs/1708.04485)                                                                                                                                   |||
  | [Going Deeper in Spiking Neural Networks: VGG and Residual Architectures](https://www.frontiersin.org/articles/10.3389/fnins.2019.00095/full)                                                                                                  |||
  | [Sparsity-Aware and Re-configurable NPU Architecture for Samsung Flagship Mobile SoC](https://ieeexplore.ieee.org/document/9499876)                                                                                                                                                                                                                                               |||

### Activation Pruning

| Publication                                                                                                                                              | Venue/Journal         | Notes |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----|
| [ELSA: Hardware-Software Co-design for Efficient, Lightweight Self-Attention Mechanism in Neural Networks](https://ieeexplore.ieee.org/document/9499860) | ISCA 2021             |      |
| [Sanger: A Co-Design Framework for Enabling Sparse Attention using Reconfigurable Architecture](https://dl.acm.org/doi/abs/10.1145/3466752.3480125)      | MICRO 2021            |      |
| [DOTA: detect and omit weak attentions for scalable transformer acceleration](https://dl.acm.org/doi/10.1145/3503222.3507738)                            | ASPLOS 2022           |      |

## Mixture of Experts (MoE)
No sense in listing them. There are good repos for that.
- [Awesome-Mixture-of-Experts-Papers - Collection of MoE papers](https://github.com/codecaution/Awesome-Mixture-of-Experts-Papers)
- [A collection of AWESOME things about mixture-of-experts ](https://github.com/XueFuzhao/awesome-mixture-of-experts)

## Parameter Efficient Fine-Tuning (PEFT)
| Publication                                                                                                                                | Venue/Journal                       | Notes                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|:----------------------------------|
| [Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning](https://arxiv.org/abs/2012.13255)                      |                                     | Prequisite for understanding PEFT |
| [LoRA: Low-rank adaptation of large language models](https://arxiv.org/abs/2106.09685)                                                     |||
| [Few-shot parameter-efficient finetuning is better and cheaper than in-context learning](https://arxiv.org/abs/2205.05638)                 |||
| [ComPEFT: Compression for Communicating Parameter Efficient Updates via Sparsification and Quantization](https://arxiv.org/abs/2311.13171) || Author: Collin Raffel               |

## Dynamic Model Architectures
Too much to list them all for now. refer to attacks on them.

| Publication                                                                       | Venue/Journal | Notes                                                                      |
|:----------------------------------------------------------------------------------|:--------------|:---------------------------------------------------------------------------|
| [Dynamic Neural Networks: A Survey](https://ieeexplore.ieee.org/document/9560049) |               | Good overview of all techniques in Figure 1                                |

### Channel Skipping Architectures

| Publication                                                                                           | Venue/Journal        | Notes |
|:------------------------------------------------------------------------------------------------------|:-------------|:-----|
  | [Dynamic Channel Pruning: Feature Boosting and Suppression](https://openreview.net/pdf?id=BJxh2j0qYm) | ICLR 2019    |      |
| [Channel gating neural networks](https://dl.acm.org/doi/abs/10.5555/3454287.3454456)                  | NeurIPS 2019 |      |

### Little Big Transformer

| Publication                                                                      | Venue/Journal               | Notes |
|:---------------------------------------------------------------------------------|:--------------------|:-----|
| [Speculative Decoding with Big Little Decoder](https://arxiv.org/abs/2302.07863) | NeurIPS Poster 2023 |      |
  | [Big Little Transformer Decoder](https://arxiv.org/pdf/2302.07863v2.pdf)         |                     |      |

## Latency Predictors
| Publication                                                                                                                              | Venue/Journal | Notes      |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------|:----------|
| [on-the-fly, on-chip latency predictors for Edge TPUs](https://blog.research.google/2019/08/efficientnet-edgetpu-creating.html)          |               | Google        |

## Attacks

### Sparsity
| Publication                                                                                                         | Venue/Journal | Notes      |
|:--------------------------------------------------------------------------------------------------------------------|:--------------|:----------|
| [Sponge Examples: Energy-Latency Attacks on Neural Networks](https://ieeexplore.ieee.org/abstract/document/9581273) | Euro S&P 2021 | First paper to define the goal of energy-latency attacks very clearly |
| [Energy-Latency Attacks via Sponge Poisoning](https://arxiv.org/abs/2203.08147)                                                                                                                    |||

## Language systems
| Publication                                                                                                                                           | Venue/Journal | Notes      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|:----------|
| [Sponge Examples: Energy-Latency Attacks on Neural Networks](https://ieeexplore.ieee.org/abstract/document/9581273)                                   | Euro S&P 2021 | First paper to define the goal of energy-latency attacks very clearly |
| [Bad Characters: Imperceptible NLP Attacks](https://ieeexplore.ieee.org/document/9833641)                                                             | S&P 2022      | E-L attacks are hard to do imperceptibly                                |
| [NMTSloth: understanding and testing efficiency degradation of neural machine translation systems](https://dl.acm.org/doi/10.1145/3540250.3549102)    |||

### Dynamic Model Architectures
| Publication                                                                                                                                                                                                                                  | Venue/Journal  | Notes      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------|:----------|
| [A Panda? No, It's a Sloth: Slowdown Attacks on Adaptive Multi-Exit Neural Network Inference](https://openreview.net/pdf?id=9xC2tWEwBD)                                                                                                      |||
| [ILFO: Adversarial Attack on Adaptive Neural Networks](https://ieeexplore.ieee.org/document/9156640)                                                                                                                                                                                                                                             |||
| [Dynamic Neural Network is All You Need: Understanding the Robustness of Dynamic Mechanisms in Neural Networks](https://ieeexplore.ieee.org/document/10350566)                                                                               |||
| [AntiNODE: Evaluating Efficiency Robustness of Neural ODEs](https://openaccess.thecvf.com/content/ICCV2023W/RCV/papers/Haque_AntiNODE_Evaluating_Efficiency_Robustness_of_Neural_ODEs_ICCVW_2023_paper.pdf)                                  |||
| [The Dark Side of Dynamic Routing Neural Networks: Towards Efficiency Backdoor Injection](https://openaccess.thecvf.com/content/CVPR2023/html/Chen_The_Dark_Side_of_Dynamic_Routing_Neural_Networks_Towards_Efficiency_CVPR_2023_paper.html) |||
| [GradMDM: Adversarial Attack on Dynamic Networks](https://ieeexplore.ieee.org/document/10089510)                                                                                                                                             |||

### Uncategorized
| Publication                                                                                                                                                                                                                                                | Venue/Journal | Notes      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|:----------|
| [Phantom Sponges: Exploiting Non-Maximum Suppression to Attack Deep Object Detectors](https://openaccess.thecvf.com/content/WACV2023/papers/Shapira_Phantom_Sponges_Exploiting_Non-Maximum_Suppression_To_Attack_Deep_Object_Detectors_WACV_2023_paper.pdf)                                                                                                                                                                                                                                                           |||
| [SlowLiDAR: Increasing the Latency of LiDAR-Based Detection Using Adversarial Examples](https://openaccess.thecvf.com/content/CVPR2023/html/Liu_SlowLiDAR_Increasing_the_Latency_of_LiDAR-Based_Detection_Using_Adversarial_Examples_CVPR_2023_paper.html) |||
| [Manipulating SGD with Data Ordering Attacks](https://proceedings.neurips.cc/paper/2021/hash/959ab9a0695c467e7caf75431a872e5c-Abstract.html)                                                                                                               | NeurIPS 2021  ||
| [NICGSlowDown: Evaluating the Efficiency Robustness of Neural Image Caption Generation Models](https://arxiv.org/abs/2203.15859)                                                                                                                           |||
---
title: Uncertainty-aware localization microscopy by variational diffusion
title_zh: 基于变分扩散的不确定性感知定位显微术
authors: "Seitz, C., Liu, J."
date: 2026-05-05
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.01.722206v1.full.pdf"
tags: ["query:smalldet"]
score: 6.5
evidence: 稠密图像中的荧光分子定位
tldr: 本文针对单分子定位显微中密集荧光图像定位存在多解与不确定性的问题，提出条件变分扩散模型（CVDM）用于核密度估计，通过对高分辨率分布的建模既提升了超分辨率成像质量，又实现了定位结果不确定性表达，显著改善了图像恢复性能。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统基于深度学习的定位显微方法无法有效表达对密集图像中分子定位的不确定性。
method: 研究采用条件变分扩散模型（CVDM），通过在低分辨率测量上训练以生成高分辨率核密度估计分布。
result: 该方法实现了高保真局部化成像，并能量化核密度估计的不确定性，优于现有模型。
conclusion: 提出的CVDM框架能提供高保真超分辨率成像和可靠的不确定性估计，对单分子及超分辨荧光显微成像具有重要意义。
---

## 摘要
利用深度神经网络从图像中快速提取物理相关信息，已经在荧光显微镜及其生物系统研究应用中取得了显著进展。例如，将深度网络用于单分子定位显微镜（SMLM）中的核密度（KD）估计，加速了细胞中高密度标记结构的超分辨成像。然而，在高密度图像中定位荧光分子是一个复杂的反问题，通常可能存在多个解。为对该问题的解的概率分布进行建模，我们提出了一种基于条件变分扩散模型（Conditional Variational Diffusion Model，CVDM）的核密度估计生成建模框架。在该框架中，CVDM通过对高分辨率KD估计分布进行建模，训练在低分辨率测量上执行定位任务。该方法使我们能够探查KD估计分布的结构并表达不确定性，而当前的深度模型在定位显微镜中尚无法实现这一点。我们证明，该模型能够实现高保真度的超分辨成像，支持对回归KD估计的不确定性评估，并在单分子及超分辨显微成像的图像恢复中具有重要意义。

## Abstract
Fast extraction of physically relevant information from images using deep neural networks has led to significant advances in fluorescence microscopy and its application to the study of biological systems. For example, the application of deep networks for kernel density (KD) estimation in single-molecule localization microscopy (SMLM) has accelerated super-resolution imaging of densely labeled structures in the cell. However, localization of fluorescent molecules in dense images is a difficult inverse problem with potentially multiple solutions. To model a probability distribution of solutions to this problem, we propose a generative modeling framework for KD estimation in SMLM based on a conditional variational diffusion model (CVDM). In this framework, CVDM is trained to perform localization tasks on low-resolution measurements by modeling a distribution of high-resolution KD estimates. This approach allows us to probe the structure of the distribution on KD estimates and express uncertainty, which is not currently offered by existing deep models for localization microscopy. We demonstrate that this model permits high-fidelity super-resolution, enables the uncertainty estimation of regressed KD estimates, and has important implications for image restoration in single-molecule and super resolution microscopy.
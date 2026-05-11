---
title: "HiReS: A Method for Automated Morphometric Trait Extraction from High-Resolution Plankton Images"
title_zh: HiReS：一种从高分辨率浮游生物图像中自动提取形态测度性状的方法
authors: "Mavrianos, S., Teurlincx, S., Declerck, S. A., Otte, K. A."
date: 2026-04-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.11.717915v1.full.pdf"
tags: ["query:yolo-mini"]
score: 8.5
evidence: 在全分辨率浮游生物图像中使用基于YOLO的实例分割。
tldr: 为提升浮游生物性状分析的自动化与效率，作者提出HiReS工作流，通过分块高分辨率图像并基于YOLO模型进行实例分割与几何特征提取，实现了形态学特征的高精度自动量化，结果显示与手工测量高度一致且具可重复性。
source: biorxiv
selection_source: fresh_fetch
motivation: 研究旨在解决传统手工测量浮游生物形态特征效率低、难以处理高分辨率图像的问题。
method: HiReS通过图像分块、YOLO实例分割和多步骤后处理生成完整的形态学特征数据。
result: 自动化测量结果与人工一致性强，能准确重现性状分布结构并在低采样下优于人工估计。
conclusion: HiReS为浮游生物高分辨率图像特征提取提供了自动化、准确且可重复的方案。
---

## 摘要
以性状为基础的浮游生态分析需要来自大量个体的测量数据，但形态测度数据通常仅从小样本中手动收集。尽管深度学习方法能够实现自动检测与分割，但由于内存限制，从高分辨率图像中提取定量性状数据仍具挑战性。我们提出了 HiReS（High-Resolution Segmentation，高分辨率分割），这是一种用于从大型浮游生物图像中自动提取形态测度性状的开源工作流程。HiReS 将图像划分为重叠的小块，使用基于 YOLO 的实例分割方法，在全图空间中重建多边形标注，去除截断和重复检测，并计算几何描述符。我们使用手动标注和自动分割结果对 HiReS 进行了评估，测试对象包括 Daphnia pulex、Daphnia galeata 和 Simocephalus vetulus。自动测量结果再现了手动性状分布的结构，在样本和个体层面均表现出高度一致性。观察到一致的正偏差，表明其反映的是乘性尺度偏移，而非性状结构的失真。进一步的子抽样分析显示，在采样深度较低时，模型得出的中位数值可优于手动估计。HiReS 提供了一种可复现且计算高效的框架，用于从高分辨率浮游生物图像中提取形态测度性状。

## Abstract
Trait-based analyses in plankton ecology require measurements from large numbers of individuals, yet morphometric data are typically collected manually from small subsets. Although deep learning methods enable automated detection and segmentation, extracting quantitative trait data from full-resolution images remains challenging due to memory limitations. We present HiReS (High-Resolution Segmentation), an open-source workflow for automated morphometric trait extraction from large plankton images. HiReS partitions images into overlapping chunks, performs YOLO-based instance segmentation, reconstructs polygon annotations in full-image space, removes truncated and duplicate detections, and computes geometric descriptors. We evaluated the workflow using manually annotated and automated segmentations of Daphnia pulex, Daphnia galeata, and Simocephalus vetulus. Automated measurements reproduced the structure of manual trait distributions and showed strong agreement at both sample and individual levels. A consistent positive bias was observed, reflecting a multiplicative scaling offset rather than distortion of relative trait structure. Subsampling analyses further showed that model-derived medians can outperform manual estimates at low sampling depths. HiReS provides a reproducible and computationally efficient framework for extracting morphometric traits from full-resolution plankton images.
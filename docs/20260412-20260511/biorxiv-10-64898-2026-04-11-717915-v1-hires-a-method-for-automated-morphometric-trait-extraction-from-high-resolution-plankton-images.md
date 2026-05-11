---
title: "HiReS: A Method for Automated Morphometric Trait Extraction from High-Resolution Plankton Images"
title_zh: HiReS：一种从高分辨率浮游生物图像中自动提取形态度量性状的方法
authors: "Mavrianos, S., Teurlincx, S., Declerck, S. A., Otte, K. A."
date: 2026-04-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.11.717915v1.full.pdf"
tags: ["query:yolo-mini"]
score: 8.5
evidence: 基于YOLO的高分辨率图像中微小浮游生物实例分割
tldr: 本研究提出HiReS，一种用于从高分辨率浮游生物图像中自动提取形态特征的开源工作流程。该方法基于YOLO分割与图像分块重组，实现高效的形态数据提取，并在多种浮游生物上验证了结果与人工测量的一致性，显著提升大规模生态分析的可行性。
source: biorxiv
selection_source: fresh_fetch
motivation: 由于形态数据通常由人工采集且耗时，亟需自动化提取高分辨率浮游生物形态特征。
method: 该方法将图像分块处理，利用YOLO进行实例分割并重构全图标注，去除误检并计算几何描述符。
result: 自动化测量结果在样本及个体层面与人工一致，呈现可解释的正偏差，并在低采样情况下更稳定。
conclusion: HiReS为高分辨率浮游生物图像的形态特征提取提供了可重复、计算高效的解决方案。
---

## 摘要
在浮游生物生态学中，基于性状的分析需要大量个体的测量数据，但形态度量数据通常仅从少量子样本中手动收集。尽管深度学习方法能够实现自动检测与分割，但由于内存限制，从高分辨率图像中提取定量性状数据仍然具有挑战性。我们提出了 HiReS（High-Resolution Segmentation，高分辨率分割），一个用于从大型浮游生物图像中自动提取形态度量性状的开源工作流程。HiReS 将图像划分为重叠块，基于 YOLO 进行实例分割，在完整图像空间中重建多边形标注，去除被截断和重复的检测对象，并计算几何描述符。我们使用人工标注和自动分割的三种浮游生物——Daphnia pulex、Daphnia galeata 和 Simocephalus vetulus——对该工作流程进行了评估。自动测量结果再现了手动性状分布的结构，并在样本和个体层面上表现出高度一致性。观察到的持续正偏差反映的是一个乘性尺度偏移，而非相对性状结构的失真。进一步的子采样分析表明，在较低采样深度下，模型推导的中位数可优于手动估计。HiReS 提供了一个可重复且计算高效的框架，用于从高分辨率浮游生物图像中提取形态度量性状。

## Abstract
Trait-based analyses in plankton ecology require measurements from large numbers of individuals, yet morphometric data are typically collected manually from small subsets. Although deep learning methods enable automated detection and segmentation, extracting quantitative trait data from full-resolution images remains challenging due to memory limitations. We present HiReS (High-Resolution Segmentation), an open-source workflow for automated morphometric trait extraction from large plankton images. HiReS partitions images into overlapping chunks, performs YOLO-based instance segmentation, reconstructs polygon annotations in full-image space, removes truncated and duplicate detections, and computes geometric descriptors. We evaluated the workflow using manually annotated and automated segmentations of Daphnia pulex, Daphnia galeata, and Simocephalus vetulus. Automated measurements reproduced the structure of manual trait distributions and showed strong agreement at both sample and individual levels. A consistent positive bias was observed, reflecting a multiplicative scaling offset rather than distortion of relative trait structure. Subsampling analyses further showed that model-derived medians can outperform manual estimates at low sampling depths. HiReS provides a reproducible and computationally efficient framework for extracting morphometric traits from full-resolution plankton images.
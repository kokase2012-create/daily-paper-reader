---
title: "LIME: a fully automated pipeline for high-throughput quantification of leaf lesions"
authors: "Tan, D."
date: 2026-05-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.07.723432v1.full.pdf"
tags: ["query:yolo-mini"]
score: 6.0
evidence: 叶片小病斑的分割与面积估算
tldr: LIME是一个利用SAM和CNN进行叶片病斑定量分析的自动化流水线。
source: biorxiv
selection_source: fresh_fetch
motivation: 叶片小病斑的分割与面积估算。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
Accurate quantification of leaf lesion severity is essential for plant disease research and phenotyping but is often limited by subjective visual scoring and time-intensive manual image analysis. We present LIME, a fully automated, open-source image analysis pipeline for high-throughput quantification of leaf lesions from disease assay images. LIME integrates zero-shot leaf segmentation using the Segment Anything Model with a convolutional neural network for lesion area estimation. Applied to Arabidopsis thaliana leaves infected with Sclerotinia sclerotiorum, the proposed approach achieved a mean absolute percentage error of 12.9%, comparable to observed intrarater variability in manual scoring. Stratified evaluation across lesion-size groups demonstrated consistent prediction accuracy for small, intermediate, and large lesions, and comparative analysis showed that the deep learning-based model substantially outperformed color-based baseline methods. Under GPU-accelerated execution, LIME processed complete assays containing approximately 200 leaves in 15 minutes, representing an approximate 13-fold reduction in processing time relative to manual annotation. Together, these results indicate that LIME enables objective, reproducible, and scalable quantification of leaf lesion severity in standardized plant pathology assays. The pipeline is released as an open-source tool to support quantitative phenotyping studies.
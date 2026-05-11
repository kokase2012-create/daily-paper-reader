---
title: Multi-Scale Contextual Attention for Robust Crop and Pest Image Classification
title_zh: 用于鲁棒农作物与害虫图像分类的多尺度上下文注意力
authors: "Majid, M., Tariq, H., Mumtaz, I., Kashif, M."
date: 2026-04-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.24.720764v1.full.pdf"
tags: ["query:yolo"]
score: 8.5
evidence: 针对作物图像中小尺寸或低对比度病症的多尺度上下文注意力机制
tldr: 本研究为解决田间作物与害虫图像因杂乱及尺度变化导致的识别困难，提出基于ResNet‑50的多尺度上下文注意（MSCA）模型，通过轻量级多尺度特征融合与联合注意机制提高鲁棒性，在新建数据集上显著超越主流模型，提升了农业图像分类的可靠性。
source: biorxiv
selection_source: fresh_fetch
motivation: 针对田间图像中背景杂乱、遮挡、光照变化和尺度差异导致的识别可靠性下降问题。
method: 采用ResNet‑50骨干网络并加入多尺度上下文注意（MSCA）模块，通过残差融合实现多尺度特征聚合与通道空间联合注意。
result: "在包含21,404张图像的测试集中，本方法达到约0.93的准确率和0.94的宏平均F1分数，优于多种现有基线模型。"
conclusion: 轻量级多尺度上下文注意机制显著提升了真实田间条件下的作物和害虫识别性能。
---

## 摘要
基于图像的农作物和害虫识别被认为有助于减少人工田间勘察的时间延迟和成本，从而支持精准农业流程中的及时干预。然而，真实田间图像仍面临诸多挑战，如背景杂乱、遮挡、光照变化以及跨作物普遍存在的强尺度变化。病症往往较小或对比度低，害虫可能部分被遮挡，这在非受控环境下会降低识别的可靠性。本文提出了一个统一的多类别农作物—害虫/病况识别框架，其中采用ResNet-50作为骨干网络，并结合多尺度上下文注意力（MSCA）模块进行了增强。其创新主要体现在通过残差融合的方式，将显式多尺度上下文聚合与轻量级的联合通道和空间注意力相结合，同时在一个固定且可复现的协议下进行受控的实证评估。本文整理了一个包含21,404张田间风格图像的数据集，涵盖15类作物和害虫/病况类别，并采用了一个具备防泄漏机制的固定划分及独立测试集以支持结果复现。仅在训练子集上应用数据增强以提高鲁棒性，而验证集未以相同方式增强。在独立测试集上，所提出的方法取得了平衡的表现，准确率约为0.93，宏平均F1得分接近0.94，并在相同评估条件下优于EfficientNet、Vision Transformer以及基于注意力的CNN等已有基线模型。通过受控消融实验，在相同训练配置下分析了MSCA和数据增强的贡献。结果表明，轻量级多尺度上下文注意力对于真实田间条件下的作物与害虫识别是有效的，尽管部分视觉上相似的类别仍较难区分。

## Abstract
Image-based crop and pest recognition is considered useful for reducing the delay and cost of manual field scouting, therefore supporting timely intervention in precision-agriculture workflows. However, the real field imagery remains challenging due to the cluttered backgrounds, occlusions, illumination changes, and strong scale variation that are frequently observed across crops. The symptoms are often small or low-contrast, and pests may be partially hidden, which reduces the reliability when the setting is outside controlled environments. A unified multi-class crop-pest/condition recognition framework is presented, where a ResNet-50 backbone is utilized and enhanced with a Multi-Scale Contextual Attention (MSCA) module. The novelty is mainly considered to be achieved through the integration of explicit multi-scale contextual aggregation with lightweight joint channel and spatial attention by means of residual fusion, while the empirical evaluation was kept controlled under a fixed and reproducible protocol. A curated dataset of 21,404 field-style images covering 15 crop and pest/condition classes was compiled, and a leakage-aware fixed split with a held-out test set was adopted to support reproducibility. Augmentation was applied only to the training subset to improve robustness, although the validation data was not augmented in the same manner. On the held-out test set, balanced performance was achieved by the proposed approach, with about 0.93 accuracy and a macro-F1 score close to 0.94 being obtained, while established baselines such as EfficientNet, Vision Transformer, and attention-based CNN models were outperformed under identical evaluation settings. Controlled ablations were used to isolate the contribution of MSCA and augmentation under the same training configuration. These results indicate that lightweight multi-scale contextual attention is effective for crop and pest recognition under realistic field conditions, although some visually similar classes remained difficult.
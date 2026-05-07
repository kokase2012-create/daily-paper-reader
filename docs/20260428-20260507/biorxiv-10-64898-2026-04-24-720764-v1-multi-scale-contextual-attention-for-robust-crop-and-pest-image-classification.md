---
title: Multi-Scale Contextual Attention for Robust Crop and Pest Image Classification
title_zh: 用于鲁棒作物与害虫图像分类的多尺度上下文注意力
authors: "Majid, M., Tariq, H., Mumtaz, I., Kashif, M."
date: 2026-04-28
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.24.720764v1.full.pdf"
tags: ["query:smalldet"]
score: 7.0
evidence: 识别微小或低对比度的病虫害特征
tldr: 本文针对田间作物与病虫识别中背景复杂、尺度变化等问题，提出一种基于ResNet-50并引入多尺度上下文注意力模块（MSCA）的统一分类框架。该方法通过轻量化的通道与空间注意力融合提升模型鲁棒性，在自建数据集上取得显著优于主流模型的性能表现。
source: biorxiv
selection_source: fresh_fetch
motivation: 为解决真实田间环境下图像中背景杂乱、尺度变化大和遮挡等因素导致的作物与病虫识别困难问题。
method: 采用基于ResNet-50的多尺度上下文注意力模块（MSCA），融合通道与空间注意力进行残差特征聚合。
result: "在21,404张野外图像的固定测试集上获得约0.93的准确率和0.94的宏平均F1值，优于多种主流模型。"
conclusion: 轻量级多尺度上下文注意力能够显著提升作物与病虫图像分类的鲁棒性，但仍有部分相似类别较难区分。
---

## 摘要
基于图像的作物和害虫识别被认为有助于减少人工田间勘查的延迟和成本，从而支持精准农业工作流程中的及时干预。然而，真实田间图像面临着显著挑战，例如复杂的背景、遮挡、光照变化以及作物间常见的强尺度变化。病害症状通常较小或对比度低，害虫也可能部分被遮挡，这在非受控环境中会降低识别的可靠性。本文提出了一个统一的多类别作物-害虫/状况识别框架，采用了ResNet-50作为主干网络，并通过一种多尺度上下文注意力（Multi-Scale Contextual Attention，MSCA）模块进行增强。该方法的新颖性主要体现在通过残差融合的方式，将显式多尺度上下文聚合与轻量级的通道和空间联合注意力相结合，同时在固定且可复现的实验协议下保持了严格控制的实证评估。研究者构建了一个包含21,404张田间风格图像的数据集，覆盖15个作物和害虫/状况类别，并采用考虑信息泄漏的固定划分和独立的测试集以确保结果的可复现性。仅对训练子集进行了数据增强以提高鲁棒性，而验证数据未采用相同的增强方式。在独立测试集上，所提出的方法取得了平衡的性能，准确率约为0.93，macro-F1得分接近0.94，并在相同评估条件下优于EfficientNet、Vision Transformer和基于注意力的CNN等已建立的基线模型。通过受控的消融实验分析了MSCA模块和数据增强在相同训练配置下的贡献。这些结果表明，轻量级多尺度上下文注意力在真实田间环境下对于作物和害虫识别具有有效性，尽管一些视觉上相似的类别仍然存在识别困难。

## Abstract
Image-based crop and pest recognition is considered useful for reducing the delay and cost of manual field scouting, therefore supporting timely intervention in precision-agriculture workflows. However, the real field imagery remains challenging due to the cluttered backgrounds, occlusions, illumination changes, and strong scale variation that are frequently observed across crops. The symptoms are often small or low-contrast, and pests may be partially hidden, which reduces the reliability when the setting is outside controlled environments. A unified multi-class crop-pest/condition recognition framework is presented, where a ResNet-50 backbone is utilized and enhanced with a Multi-Scale Contextual Attention (MSCA) module. The novelty is mainly considered to be achieved through the integration of explicit multi-scale contextual aggregation with lightweight joint channel and spatial attention by means of residual fusion, while the empirical evaluation was kept controlled under a fixed and reproducible protocol. A curated dataset of 21,404 field-style images covering 15 crop and pest/condition classes was compiled, and a leakage-aware fixed split with a held-out test set was adopted to support reproducibility. Augmentation was applied only to the training subset to improve robustness, although the validation data was not augmented in the same manner. On the held-out test set, balanced performance was achieved by the proposed approach, with about 0.93 accuracy and a macro-F1 score close to 0.94 being obtained, while established baselines such as EfficientNet, Vision Transformer, and attention-based CNN models were outperformed under identical evaluation settings. Controlled ablations were used to isolate the contribution of MSCA and augmentation under the same training configuration. These results indicate that lightweight multi-scale contextual attention is effective for crop and pest recognition under realistic field conditions, although some visually similar classes remained difficult.
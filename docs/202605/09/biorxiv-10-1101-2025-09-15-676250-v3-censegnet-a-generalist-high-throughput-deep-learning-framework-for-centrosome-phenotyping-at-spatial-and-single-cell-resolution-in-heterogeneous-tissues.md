---
title: "CenSegNet: a generalist high-throughput deep learning framework for centrosome phenotyping at spatial and single-cell resolution in heterogeneous tissues"
title_zh: CenSegNet：一种用于异质组织中具空间和单细胞分辨率的中心体表型分析的通用高通量深度学习框架
authors: "Cheng, J., Fan, K., Bailey, M., Du, X., Jena, R., Savva, C., Reed, E., Gou, M., Zuo, P., Beers, S., Cutress, R., Cai, X., Elias, S."
date: 2026-05-04
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.15.676250v3.full.pdf"
tags: ["query:smalldet"]
score: 7.0
evidence: 对中心体（微小细胞结构）进行高分辨率分割
tldr: 本研究提出CenSegNet深度学习框架，用于高分辨率解析组织中中心体异常特征。通过在乳腺癌组织微阵列中大规模应用，该模型实现了单细胞水平的精确分割与定量，揭示了中心体异常的空间模式、临床相关性及对患者预后的指示价值。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统图像分析难以解析组织中中心体异常的空间复杂性与表型异质性。
method: 构建了双分支架构并结合不确定性引导的深度学习框架CenSegNet，实现高精度中心体及上皮结构分割。
result: CenSegNet在多种组织类型和成像方式上表现优异，并揭示了不同类型中心体异常的空间分布与临床指标相关。
conclusion: CenSegNet为解析癌症中中心体异常提供了新的空间分辨工具，并具备临床相关性和广泛适用性。
---

## 摘要
中心体异常（CA）是上皮癌的标志之一，但由于传统图像分析的限制，其空间复杂性和表型异质性尚未得到充分解析。我们提出了 CenSegNet（Centrosome Segmentation Network，中心体分割网络），这是一个模块化的深度学习框架，用于在各种组织类型中对中心体和上皮结构进行高分辨率、上下文感知的分割。CenSegNet 结合双分支架构与基于不确定度的精化机制，在免疫荧光与免疫组织化学两种成像方式中均实现了最先进的性能和通用性，在准确度与形态保真度上超越现有模型。应用于包含来自 127 名患者的 911 个乳腺癌组织芯片样本的组织微阵列（TMA）时，CenSegNet 实现了首个在单细胞分辨率下空间解析的数值与结构性 CA 的大规模定量分析。这些 CA 亚型在机制上相互独立，表现出不同的空间分布、年龄相关动态以及与组织学肿瘤分级、激素受体状态、基因组改变和淋巴结受累的关联。结构性 CA 水平还与总体生存率相关，支持空间解析 CA 模式的临床相关性。肿瘤边缘的 CA 失配特征与局部侵袭性及基质重塑相关。为促进广泛应用与可重复性，CenSegNet 已作为开源 Python 库发布。总体而言，我们的研究确立了 CenSegNet 作为一种可扩展且具有广泛通用性的空间解析中心体表型分析平台，可系统性地研究该细胞器的生物学及其在癌症和其他上皮性疾病中的失调。

## Abstract
Centrosome abnormalities (CA) are a hallmark of epithelial cancers, yet their spatial complexity and phenotypic heterogeneity remain poorly resolved due to limitations in conventional image analysis. We present CenSegNet (Centrosome Segmentation Network), a modular deep learning framework for high-resolution, context-aware segmentation of centrosomes and epithelial architecture across diverse tissue types. Integrating a dual-branch architecture with uncertainty-guided refinement, CenSegNet achieves state-of-the-art performance and generalisability across both immunofluorescence and immunohistochemistry modalities, outperforming existing models in accuracy and morphological fidelity. Applied to tissue microarrays (TMAs) containing 911 breast cancer sample cores from 127 patients, CenSegNet enables the first large-scale, spatially resolved quantification of numerical and structural CA at single-cell resolution. These CA subtypes are mechanistically uncoupled, exhibiting distinct spatial distributions, age-dependent dynamics, and associations with histological tumour grade, hormone receptor status, genomic alterations, and nodal involvement. Structural CA levels are additionally associated with overall survival, supporting the clinical relevance of spatially resolved CA patterns. Discordant CA profiles at tumour margins are linked to local aggressiveness and stromal remodelling. To support broad adoption and reproducibility, CenSegNet is released as an open-source Python library. Together, our findings establish CenSegNet as a scalable, generalisable platform for spatially resolved centrosome phenotyping in intact tissues, enabling systematic dissection of the biology of this organelle and its dysregulation in cancer and other epithelial diseases.
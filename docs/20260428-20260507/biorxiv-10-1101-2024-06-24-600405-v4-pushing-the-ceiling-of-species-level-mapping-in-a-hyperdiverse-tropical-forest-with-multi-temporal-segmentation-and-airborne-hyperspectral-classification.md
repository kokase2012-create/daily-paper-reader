---
title: Pushing the ceiling of species-level mapping in a hyperdiverse tropical forest with multi-temporal segmentation and airborne hyperspectral classification
title_zh: 通过多时相分割和机载高光谱分类在高多样性热带森林中提升物种级制图上限
authors: "Ball, J. G. C., Jaffer, S., Laybros, A., Prieur, C., Jackson, T. D., Madhavapeddy, A., Barbier, N., Vincent, G., Coomes, D."
date: 2026-05-05
pdf: "https://www.biorxiv.org/content/10.1101/2024.06.24.600405v4.full.pdf"
tags: ["query:smalldet"]
score: 6.0
evidence: 从无人机RGB调查中描绘单个树冠
tldr: "本研究针对法属圭亚那高多样性湿热带森林，通过多时序无人机RGB树冠分割与航空高光谱分类相结合，实现了约70%的树冠物种准确映射，显著提升了分割与分类精度，对森林生物多样性遥感监测具有重要意义。"
source: biorxiv
selection_source: fresh_fetch
motivation: 鉴于热带森林物种丰富和结构复杂，探索提升物种级遥感分类精度以改进生物多样性监测与保护规划。
method: 采用多时序无人机RGB影像通过Mask R-CNN进行树冠分割，并以远程航空高光谱数据结合多种机器学习模型进行物种分类。
result: "多时序融合使树冠分割F1提高至0.78，LDA分类加权F1达0.75，整体约70%树冠面积正确映射至物种。"
conclusion: 研究表明多时序树冠分割结合高光谱分类可显著提升物种级森林映射精度，但在稀有物种和跨区域泛化方面仍有限。
---

## 摘要
热带森林树冠的物种级地图对于生物多样性监测、保护规划和碳核算至关重要，但这些森林的结构复杂性和物种丰富度使得遥感分类充满挑战。本文评估了一种应用于法属圭亚那 Paracou 野外站高多样性湿润森林的两步制图方法的极限与潜力。首先，我们利用卷积神经网络 (Mask R-CNN) 从十次重复的无人机 RGB 调查中分割出单株树冠，并通过时间一致性融合方法整合不同时间的预测，使平均分割 F1 值从单日的 0.68 提升至十日的 0.78，覆盖了约 86% 的树冠面积。其次，我们使用一次机载高光谱图像（416–2500 nm，1 m 分辨率）对每个树冠进行物种分类，采用多种机器学习分类器进行训练和测试，基于 3,186 个经过实地验证的树冠，涵盖 169 种物种（来自一个共 3,256 个树冠、239 种物种的标注库）。线性判别分析（LDA）获得了最高的分类准确率（加权 F1 = 0.75），但性能分布不均：重复交叉验证（20 × 5 折）结果表明，平均每次验证中约有 50 种物种（95% 置信区间：41–63）的 F1 ≥ 0.7，其中 38 种在平均水平上保持这一表现，15 种在超过 80% 的折次中始终达到这一标准，而少数样本较少的稀有物种仍无法有效分类（宏平均 F1 = 0.48）。结合分割与分类结果，我们估算约有 70% 的景观树冠面积实现了正确的物种映射。波段重要性与消融分析表明，远红边（748–775 nm）是信息量最丰富的光谱区域，而红光、绿光和短波红外（SWIR）则提供次要贡献。尽管本研究的成果相较于此前仅识别不足 20 种物种的研究有显著提升，我们仍警告分类精度高度依赖于训练数据的充足性、站点特定的光谱条件及单次采集设计，其对其他地区和传感器的泛化能力尚需验证。

## Abstract
Species-level maps of tropical forest canopies are needed for biodiversity monitoring, conservation planning, and carbon accounting, yet the structural complexity and species richness of these forests make remote classification challenging. Here we evaluate the limits and possibilities of a two-step mapping approach applied to hyperdiverse moist forest at the Paracou Field Station, French Guiana. First, we delineate individual tree crowns from ten repeat UAV RGB surveys using a CNN (Mask R-CNN) and combine predictions across dates via a temporal consensus-fusion method, improving mean segmentation F1 from 0.68 (single date) to 0.78 (ten dates) and covering approximately 86% of canopy area. Second, we classify the species of each crown from a single airborne hyperspectral acquisition (416--2500 nm, 1 m resolution) using several machine learning classifiers trained and tested on 3,186 field-verified crowns spanning 169 species (drawn from a labelled pool of 3,256 crowns across 239 species; see \cref{sec:representative_tree_species_classificati}). Linear Discriminant Analysis (LDA) achieved the highest accuracy (weighted F1 = 0.75), though performance was uneven: repeated cross-validation (20 x 5-fold) showed that on average 50 species (95% CI: 41--63) attained F1 >= 0.7 in any given fold, with 38 maintaining this level on average and 15 doing so reliably (>= 80% of folds), while many rare species with few training examples remained unclassifiable (macro-average F1 = 0.48). Combining segmentation and classification, we estimate that approximately 70% of the landscape's canopy area was correctly mapped to species. Band-importance and ablation analyses identified the far-red edge (748--775 nm) as the most informative spectral region, with secondary contributions from the red, green, and SWIR. While these results represent a substantial advance over previous studies limited to fewer than 20 species, we caution that accuracy is strongly conditioned by training data availability, site-specific spectral conditions, and the single-acquisition design, and that generalization to other sites and sensors remains to be demonstrated.
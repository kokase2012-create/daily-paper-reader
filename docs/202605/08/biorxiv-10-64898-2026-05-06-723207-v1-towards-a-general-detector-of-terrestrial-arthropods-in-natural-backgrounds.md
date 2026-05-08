---
title: Towards a general Detector of terrestrial Arthropods in Natural backgrounds
title_zh: 迈向一种在自然背景下通用的陆生节肢动物检测器
authors: "Remy, E., Carlier, A., Massol, E., Kacimi, R., Chaine, A. S., Cauchoix, M."
date: 2026-05-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.06.723207v1.full.pdf"
tags: ["query:smalldet"]
score: 7.0
evidence: 在自然背景下检测小型陆生节肢动物
tldr: 研究针对节肢动物数量下降的生态风险，提出一种可广泛应用的自动检测方法。团队构建了覆盖法国所有陆生节肢动物科的图像数据集，并采用迭代训练的YOLOv11模型实现高精度检测（F1=0.91），显著提升了在自然场景下的泛化能力，助力生态监测与公民科学项目。
source: biorxiv
selection_source: fresh_fetch
motivation: 由于节肢动物数量下降带来生态与农业风险，需要标准化、可扩展的图像监测与自动检测方法。
method: 研究通过迭代使用YOLOv11模型预标注、人工校正和再训练，构建了覆盖法国所有陆生节肢动物科的检测数据集。
result: 最终模型在自然场景下节肢动物检测任务中F1值达0.91，并能很好泛化至未见物种、科和背景。
conclusion: 该研究推动了在自然背景下自动化节肢动物图像分析，为生态监测和公民科学提供可扩展的工具。
---

## 摘要
节肢动物的广泛衰退对生态系统功能和农业构成风险。评估这种衰退或潜在的恢复需要标准化且可扩展的种群监测。基于图像的方法（如相机陷阱和公民科学项目）被越来越多地使用，但收集到的大量数据需要自动化分析。稳健的节肢动物检测对于个体计数或细粒度分类至关重要，但现有的数据集和算法尚未解决节肢动物物种间巨大的形态多样性，也常忽视了节肢动物被拍摄时的背景、光照和图像构图等摄影语境的多样性。为填补这一空白，我们构建了一个节肢动物检测数据集，覆盖法国境内在 iNaturalist 平台上有验证图像的全部陆生节肢动物科（共 749 科）。为实现这一目标，我们采用了迭代工作流程：使用 YOLOv11 模型对每科代表物种的图像进行预标注，随后进行人工校正并重新训练模型。重复此过程逐步减少了标注工作量并提高了模型准确性。最终成果包括一个公开可用的精炼检测数据集，以及一个适用于自然背景场景的稳健节肢动物检测器。该检测器的 F1 分数达到 0.91，显示出在物种间显著形态差异和摄影语境异质性下仍具强劲性能。我们进一步展示了模型的分类学普适性，在纲（F1=0.79，IoU=0.85）和目（F1=0.82，IoU=0.86）层面均表现出高分数，并且在模型训练期间未遇到的物种、属和科上也取得了良好的检测泛化能力（F1>0.90，IoU>0.83）。最后，我们展示了如何通过数据增强、补充训练数据或微调来提高模型在新数据集上的泛化能力及小目标检测性能。特别地，我们报告了改进模型在三种常用于非致死性昆虫监测的应用场景中的表现：(i) 通过公民科学进行的昼行传粉者监测；(ii) 通过智能手机对紫外光照白板的延时拍摄进行花上与夜行昆虫监测。这些结果标志着在自然场景下实现节肢动物图像自动化分析的重要一步，无论是在大规模自动监测方法还是公民科学监测项目中。

## Abstract
Widespread arthropod declines pose risks to ecosystem functioning and agriculture. Assessing this decline or potential remediation implies the need for standardized and scalable population monitoring. Image-based methods, including camera traps and citizen science programs, are increasingly used, but the volume of data collected requires automated analysis. Robust arthropod detection is essential for individual counting or fine-grained classification, yet current datasets and algorithms do not address the vast morphological diversity across arthropod species and often overlook the variety of photographic contexts, such as differences in background, lighting, and image composition, in which arthropods are captured. To address this gap, we developed an arthropod detection dataset, covering all terrestrial families present in France with available validated images on the iNaturalist platform (749 families). To achieve this, we employed an iterative workflow in which a YOLOv11 model pre-annotated images - using one representative species per family - followed by manual correction and model retraining. Repeating this process progressively reduced annotation effort and improved model accuracy. The final outcome consists of a publicly available curated detection dataset and a robust arthropod detector for natural background scenes. The detector achieves an F1-score of 0.91, demonstrating strong performance despite substantial interspecific morphological variation and heterogeneity in photographic contexts. We further demonstrated the taxonomical universality of the model showing high F1-score and IoU averaged at the class (0.79, 0.85) and order level (0.82, 0.86) and also a good detection generalizability (F1-score>0.90, IoU>0.83) on species, genera and families never encountered by the model during training. Finally, we show how this model can be improved to generalize to new datasets using data augmentation, complementary training data or fine-tuning and increase detection of small objects. In particular, we report performance of the improved models on three use cases largely used in non lethal insect monitoring: (i) diurnal pollinator monitoring through citizen science or (ii) flower and nocturnal insects monitoring through smartphone time-lapse of a UV-illuminated white panel. These results mark an important step toward automated analysis of arthropod images in natural contexts, from both large-scale automated monitoring approaches or from citizen science monitoring programs.
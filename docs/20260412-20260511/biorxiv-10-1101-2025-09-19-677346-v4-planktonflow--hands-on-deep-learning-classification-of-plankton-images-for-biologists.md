---
title: "PlanktonFlow : hands-on deep-learning classification of plankton images for biologists"
title_zh: PlanktonFlow：面向生物学家的浮游生物图像深度学习分类实操
authors: "Walter, H., Gorzerino, C., Collinet, M., Porcon, B., Martignac, F., Edeline, E."
date: 2026-04-29
pdf: "https://www.biorxiv.org/content/10.1101/2025.09.19.677346v4.full.pdf"
tags: ["query:yolo-mini"]
score: 7.5
evidence: 在浮游生物图像分类流程中包含了YOLO算法
tldr: 本文介绍了PlanktonFlow，一个为生物学家设计的Python工具，自动化完成浮游生物图像的预处理、增广、CNN模型训练和推理。通过比较四种网络架构的性能，项目发现EfficientNet-B5表现最佳，并验证了超参数优化的重要性。工具开源且易于扩展，为生物图像分类提供了高效解决方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 高通量成像设备产生的大量生物图像难以被非专家高效分析，需要一个简化深度学习实现的工具。
method: 研究开发了一个Python流水线，集成CNN训练、性能评估和推理，用于浮游生物图像分类。
result: 在淡水浮游生物图像测试中，EfficientNet-B5取得最高宏平均F1分数，表现优于其他模型和EcoTaxa。
conclusion: PlanktonFlow是一个开源且模块化的工具，可显著提升生物学家的图像分类效率，并具备良好的拓展性。
---

## 摘要
高通量的图像采集设备极大地提升了我们观察生物多样性的能力。然而，对于许多生物学家而言，理解大量图像数据所需的高性能深度学习模型仍然难以实现。

为填补生物学家工具箱中的这一空白，我们开发了 PlanktonFlow——一个基于 Python 的流程，可简化浮游生物图像分类的自动化过程。PlanktonFlow 使缺乏经验的用户能够轻松运行完整的流程，包括：(i) 自动图像预处理与稀有类别的增强，(ii) 训练最多四种高性能卷积神经网络（CNNs：ResNet、DenseNet、EfficientNet 和 YOLO），(iii) 计算模型分类性能指标以选择表现最佳的模型，以及 (iv) 对新图像集进行推理。PlanktonFlow 还包含例程，可方便地微调模型超参数并优化模型性能。

采用教程式的展示，我们演示了如何使用 PlanktonFlow 分析由 FlowCAM 生成的淡水浮游生物图像，并比较四种优化后的 CNN 架构的分类性能。为了与浮游生物学家常用的参考工具进行基准对比，我们进一步评估了 EcoTaxa 网络服务在无人工验证、纯预测模式下的分类性能。与之前在浮游生物基准数据集上的研究一致，我们发现 EfficientNet-B5 获得了最高的宏平均 F1 分数，性能超过其他 CNN 模型，且所有模型的表现均优于 EcoTaxa。超参数优化对提升模型性能至关重要。

为了方便社区的使用与进一步发展，PlanktonFlow 是开源的，附带详细的文档，并具有模块化结构。我们预计未来的工作可以集成新的深度学习架构（如视觉 Transformer、半监督学习等），并在其他设备生成的图像或其他分类群上测试该流程。

## Abstract
High throughput image-acquisition devices tremendously increase our capacity to observe biodiversity. However, for many biologists, the high-performance deep learning models that are needed to make biological sense out of very-large image sets remain difficult to implement.

To fill this gap in biologists toolkit, we developed PlanktonFlow, a Python pipeline that streamlines the automation of plankton-image taxonomic assignment. PlanktonFlow makes it easy for inexperienced users to run a whole sequence of (i) automated image pre-processing and augmentation of rare classes, (ii) training up to four different high-performance convolution neural networks (CNNs: ResNet, DenseNet, EfficientNet, and YOLO), (iii) computing model classification-performance metrics so as to choose the best-performing model, and (iv) running inference on novel image sets. PlanktonFlow further includes routines to easily fine tune model hyper-parameters and optimize models performances.

Using a tutorial style, we demonstrate the usage of PlanktonFlow to analyse freshwater-plankton images produced with the FlowCAM, comparing the relative classification performances of the four optimized CNN architectures. For a baseline comparison with a reference tool used by plankton biologists, we further assessed the classification performances of the EcoTaxa web-service when used without any eye validation in a pure-prediction mode. In line with a previous study on a benchmark plankton dataset, we found that EfficientNet-B5 achieved the highest macro-averaged F1 Score, outperforming other CNN models, which all surpassed EcoTaxa. Hyper-parameter optimization was key to improving model performances.

To ease an appropriation and further developments by the community, PlanktonFlow is open source, comes with a detailed documentation, and has a modular structure. We foresee that future work could integrate new deep-learning architectures (e.g., vision transformers, semi-supervised learning), and test the pipeline on images produced by other devices or from other taxonomic groups.
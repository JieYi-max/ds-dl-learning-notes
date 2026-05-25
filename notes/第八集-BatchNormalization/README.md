# 第八集：Batch Normalization（批次归一化）

**课程：** 機器學習2021 (李宏毅)
**标题：** 類神經網路訓練不起來怎麼辦 (五)：批次標準化
**对应课件：** `机器学习课程资源（1）/05 Transformer/课件/normalization_v4.pdf`

---

## 笔记目录

| # | 笔记 | 优先级 | 对应 PPT |
|---|---|---|---|
| 1 | [为什么需要归一化](./01-为什么需要归一化.md) | ⭐⭐⭐ | 第 2-4 页 |
| 2 | [Batch Normalization 原理](./02-BatchNormalization原理.md) | ⭐⭐⭐ | 第 5-9 页 |
| 3 | [BN 为什么有效 & 局限](./03-BN有效性与局限.md) | ⭐⭐ | 第 10-12 页 |

## 整体知识链

问题：神经网络的 error surface 崎岖不平，训练困难
  ↓
方案 1：Feature Normalization（对输入层做归一化）
  ↓
方案 2：Batch Normalization（对每一层做归一化）
  ↓
BN 为什么有效：平滑 error surface（不是 Internal Covariate Shift）
  ↓
BN 的局限：依赖 batch size → 大模型用 Layer Normalization

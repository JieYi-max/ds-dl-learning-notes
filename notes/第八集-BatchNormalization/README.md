# 第八集：Batch Normalization（批次归一化）

**课程：** 機器學習2021（李宏毅）
**标题：** 類神經網路訓練不起來怎麼辦 (五)：批次標準化
**课件：** `机器学习课程资源（1）/05 Transformer/课件/normalization_v4.pdf`

---

## 笔记列表

| # | 笔记 | 优先级 |
|---|---|---|
| 1 | [为什么需要归一化](./01-为什么需要归一化.md) | ⭐⭐⭐ |
| 2 | [Batch Normalization 原理](./02-BN原理.md) | ⭐⭐⭐ |
| 3 | [BN 为什么有效 & 局限](./03-BN有效性与局限.md) | ⭐⭐ |

## 内容路线

问题：不同特征数值范围不同，导致梯度差异大，训练困难

→ 方案1：Feature Normalization（对输入层归一化）

→ 方案2：Batch Normalization（对每一层归一化）

→ BN 本质：让 error surface 变平滑

→ BN 局限：依赖 batch size → 大模型改用 Layer Norm

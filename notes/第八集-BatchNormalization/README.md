# 第八集：Batch Normalization（批次归一化）

**课程：** 機器學習2021 (李宏毅)
**标题：** 類神經網路訓練不起來怎麼辦 (五)：批次
**对应课件：** `05 Transformer/课件/normalization_v4.pdf`

---

## 目录

| # | 笔记 | 说明 |
|---|---|---|
| 1 | [特征归一化](./01-特征归一化.md) | 为什么需要归一化 |
| 2 | [Batch Normalization](./02-BatchNormalization.md) | BN 的原理与公式 |
| 3 | [BN 的作用](./03-BN的作用.md) | BN 为什么有效 |

## 核心结论

- 输入特征尺度不一致 → 训练困难 → 需要 Feature Normalization
- 神经网络中间层的输出也会尺度不一致 → 需要 Batch Normalization
- BN = 对每个 batch 算 μ 和 σ → 归一化 → 再用 γ、β 恢复表达能力
- BN 让 error surface 更平滑，训练更快

# 视频 08：類神經網路訓練不起來怎麼辦 (二) — 批次與動量

**课程：** 機器學習2021 (李宏毅)
**链接：** https://youtu.be/BABPWOkSbLE
**主题：** Batch（批次）& Momentum（动量）

---

## 目录

| # | 笔记 | 对应视频时间 |
|---|---|---|
| 1 | [Error Surface（误差曲面）](./01-error-surface.md) | ~5:58 |
| 2 | [Batch Size 的影响](./02-batch-size.md) | 中段 |
| 3 | [Momentum（动量）](./03-momentum.md) | 后段 |

## 重点总结

- Error Surface 是模型参数与 loss 构成的"地形图"，训练就是在这张图上找最低点
- Batch size 会影响训练的稳定性、速度和泛化能力
- Momentum = 给梯度下降加惯性，帮助冲出局部最小值和平坦区域

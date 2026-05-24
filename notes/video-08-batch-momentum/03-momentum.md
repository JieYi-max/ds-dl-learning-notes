# Momentum（动量）

**优先级：⭐ 重要**

## 一句话

> **Momentum = 给梯度下降加"惯性"。更新时不仅看当前梯度方向，还带上之前的方向。**

## 公式对比

**普通 SGD**
![SGD公式](./formula_sgd.png)

**SGD + Momentum**
![Momentum公式](./formula_momentum.png)

| 符号 | 含义 | 典型值 |
|---|---|---|
| v | 速度（velocity），累积的历史方向 | 初始为 0 |
| μ | 动量系数，保留多少历史速度 | 0.9 |
| η (lr) | 学习率 | 0.01 ~ 0.0001 |
| g | 当前梯度 | 由 loss.backward() 算出 |

## 直观理解

```
没有 Momentum：
  遇到一个小坑 → 卡住 → 以为到了谷底

有 Momentum (μ=0.9)：
  当前方向 + 90% 的历史方向 → 靠惯性冲过小坑
```

## 两种困难地形

| 地形 | 无 Momentum | 有 Momentum |
|---|---|---|
| **平坦区域** | 梯度小 → 走不动 | 靠历史速度继续走 |
| **峡谷震荡** | Z 字形来回震荡 | 震荡互相抵消，走得更直 |

## 代码

```python
# 无 Momentum
optimizer = torch.optim.SGD(model.parameters(), lr=0.01)

# 有 Momentum
optimizer = torch.optim.SGD(model.parameters(), lr=0.01, momentum=0.9)
```

## 关联知识

- → 跟 Error Surface 的关系：Momentum 就是为了对付 error surface 上的小坑
- → 跟 Adam 的关系：Adam = Momentum + RMSProp

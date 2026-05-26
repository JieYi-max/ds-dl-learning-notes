# Momentum（动量）

## 核心理解

**Momentum = 给梯度下降加"惯性"**

参数更新时不仅看当前梯度方向，还带上上一次更新的方向。

## 数学公式

```
SGD:         w = w - lr × g
SGD+Momentum: v = μ × v_old - lr × g
               w = w + v
```

| 符号 | 含义 | 典型值 |
|---|---|---|
| v | 速度（velocity） | 初始为0 |
| μ | 动量系数 | 0.9 |
| lr | 学习率 | 0.01 ~ 0.0001 |
| g | 当前梯度 | 由 loss.backward() 算出 |

## 直观理解

```
没有 Momentum：遇到小坑就停住了，来回震荡
有 Momentum：靠惯性冲出小坑，走得更直更快
```

## 代码

```python
# 没有 Momentum
optimizer = torch.optim.SGD(model.parameters(), lr=0.01)

# 有 Momentum
optimizer = torch.optim.SGD(model.parameters(), lr=0.01, momentum=0.9)
```

## 优化器进化路线

```
SGD → SGD+Momentum → RMSProp → Adam → AdamW
```

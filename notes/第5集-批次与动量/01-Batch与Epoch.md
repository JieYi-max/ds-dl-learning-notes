# Batch 与 Epoch

## 核心理解

| 概念 | 含义 | 类比 |
|---|---|---|
| Epoch | 全部数据学完一轮 | 一餐饭全部吃完 |
| Batch | 一次喂多少样本 | 一口吃多少 |
| Batch Size | 一批的样本数 | 一口吃多大 |
| 更新次数 | batch数 × epoch数 | 总共咀嚼次数 |

## 形状变化
总数据: [1000, 1, 28, 28]  全部数据
  ↓ batch_size=32
每个batch: [32, 1, 28, 28]  ← 每次喂32张

## 代码骨架
python
for epoch in range(10):              # 外层：学10轮
    for x, y in dataloader:          # 内层：分批喂
        loss = model(x, y)
        loss.backward()
        optimizer.step()
## 跟部署的关系
部署时虽然没有 epoch，但 batch_size 仍然影响推理吞吐量。

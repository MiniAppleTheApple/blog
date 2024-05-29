---
title: "速度疊加"
date: 2024-05-28T18:16:14-03:00
draft: false 
---

> 這篇主要用途爲用於課業的筆記，所以有些名詞會怪怪的是正常的，我們在學校用的專有名詞是葡文的，有任何錯誤歡迎告訴我。

# Composicao de movimento 

- V relative 是行駛的速度
- V inner 是那個物體總移動的速度
- V outer 是V inner物體所在的物體的速度

這樣代表說

### 如果移動的物體和他所在的物體的方向是相同的

```
V relative = V inner + V outer
V inner = V relative + V outer
```

### 如果是相反的

```
V relative = V inner - V outer
V inner = V relative + V outer
```

### 如果方向不同

```
V relative = V inner + V outer
V inner = V relative + V outer
```

## 輪胎

當輪胎移動的時候是兩種力在推動它：平移運動和旋轉。

### 平移運動

平移運動的時候輪胎的五個點都朝着一個方向移動。

### 旋轉

假設輪胎向右邊移動：

- 上面的點向右邊移動，爲v
- 右邊的點向下移動，爲v
- 下面的點向左邊移動，爲v
- 左邊的點向上移動，爲v
- 中心的點不移動，爲0

### 融合

融合後，假設輪胎向右邊移動，每個點的力爲：

- 上面的點向右邊移動，因爲兩種力向同一個方向疊加，爲2v
- 右邊的點向右下移動，兩種力中間形成一條斜線，爲$$sqrt{2}v
- 下面的點向不移動，爲0
- 左邊的點向左上移動，兩種力中間形成一條斜線，爲$$sqrt{2}v

# 重點

- 記得a ^ 2 = b ^ 2 + c ^ 2
- [輪胎](#輪胎)

---
type: concept
title: "DCF 貼現現金流"
aliases: ["Discounted Cash Flow", "DCF估值", "貼現現金流量分析"]
tags: [財務分析, 估值, DCF, 投資, 財務報表]
source_count: 2
last_updated: 2026-11-23
---

## 定義

DCF（Discounted Cash Flow，貼現現金流）是將企業未來預期產生的自由現金流，以適當的折現率（通常為 WACC）折算回現值，以估計企業內在價值的財務估值方法。

## 核心公式

$$
V = \sum_{t=1}^{n} \frac{FCF_t}{(1+WACC)^t} + \frac{FCF_n \times (1+g)}{(WACC - g) \times (1+WACC)^n}
$$

其中：
- $FCF_t$：第 t 年自由現金流
- $WACC$：加權平均資金成本
- $g$：終端成長率

## 在星宇航空案例中的應用

| WACC \ g | 1.5% | 2.0% | 2.5% |
|----------|------|------|------|
| 9.5% | NT\$37.34 | NT\$40.21 | NT\$43.49 |
| **10.5%（基準）** | NT\$28.45 | **NT\$30.53** | NT\$32.86 |
| 11.5% | NT\$21.45 | NT\$22.99 | NT\$24.70 |

基準案例（WACC=10.5%, g=2%）：**NT\$30.53/股**

## 各來源的觀點比較

| 來源 | 應用方式 |
|------|----------|
| [[sources/2024-11_星宇航空IPO分析]] | 四情境 FCF 合併後進行 DCF，搭配 DDM 交叉驗證 |
| [[sources/2024-10_財務報表分析理論]] | 介紹 DCF 理論框架與 FCF 計算方式 |

## 相關概念

- [[concepts/WACC加權平均資金成本]]
- [[concepts/DDM股利折現模型]]
- [[concepts/自由現金流FCF]]

## 相關實體

- [[entities/星宇航空]]

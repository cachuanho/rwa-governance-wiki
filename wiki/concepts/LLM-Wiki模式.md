---
type: concept
title: "LLM Wiki 模式"
aliases: ["LLM Wiki Pattern", "個人知識庫模式", "Karpathy Wiki"]
tags: [LLM, 知識管理, Wiki, AI工具, 學習方法]
source_count: 1
last_updated: 2026-11-23
---

## 定義

LLM Wiki 模式是由 Andrej Karpathy 提出的個人知識庫建構方法：讓 LLM 擔任「書記員」，持續將新資料整合進一個結構化的 wiki 文件集合中，使知識隨時間**累積複利**，而非每次重新推導。

## 核心架構

```
原始來源（Raw Sources）→ [LLM Ingest] → Wiki 知識庫 → [LLM Query] → 答案
                                              ↑
                                      Schema（AGENTS.md）
```

## 與 RAG 的比較

| 面向 | 傳統 RAG | LLM Wiki |
|------|----------|----------|
| 知識存放 | 原始文件向量庫 | 結構化 Markdown wiki |
| 查詢時 | 即時檢索 + 生成 | 讀 index → 讀頁面 → 合成 |
| 知識積累 | ❌ 每次重新發現 | ✅ 持續累積 |
| 交叉引用 | 偶發 | 系統性建立 |
| 矛盾處理 | 被動 | 主動標注 |
| 維護成本 | 低（自動） | LLM 承擔書記工作 |

## 三大操作

1. **Ingest**：新來源 → 摘要頁 → 更新概念/實體頁 → 更新 index + log
2. **Query**：問題 → 讀 index → 讀相關頁 → 合成答案（附引用）
3. **Lint**：定期健康檢查（孤兒頁、矛盾、過時資訊）

## 相關概念

- [[concepts/RAG vs LLM-Wiki]]
- [[concepts/Ingest工作流程]]

## 相關實體

- [[entities/Obsidian]]

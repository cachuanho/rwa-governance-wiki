---
type: source
title: "Andrej Karpathy LLM Wiki：用 LLM 建立個人知識庫的模式"
date: 2026-04-01
source_type: article
author: "Andrej Karpathy"
tags: [LLM, 知識庫, Wiki, RAG, AI工具, 個人知識管理]
ingest_date: 2026-11-23
source_file: "（課程提供，非本地文件）"
---

## 摘要

Karpathy 提出以 LLM 為核心的個人知識庫建構模式，區別於傳統 RAG（檢索增強生成）系統：不是在查詢時從原始文件即時檢索，而是讓 LLM 持續建立並維護一個結構化的 wiki 文件集合，使知識「累積」而非「重新發現」。這個模式包含三層架構（原始來源、Wiki、Schema）與三大操作（Ingest、Query、Lint）。

## 重點條列

- **核心差異**：傳統 RAG 每次查詢重新從原始文件推導；LLM Wiki 是**一次整理、持續複利**的知識資產
- **三層架構**：
  1. **Raw Sources**（原始來源）：唯讀，LLM 只讀不改
  2. **Wiki**（知識庫）：LLM 完全維護，使用者只讀
  3. **Schema**（操作規範）：AGENTS.md / CLAUDE.md，定義工作流程
- **三大操作**：
  - **Ingest**：讀新來源 → 討論 → 建摘要頁 → 更新概念/實體頁 → 更新 index → 寫 log
  - **Query**：讀 index → 找相關頁 → 合成答案（有引用）→ 優質答案存回 wiki
  - **Lint**：定期健康檢查，找孤兒頁、矛盾、過時資訊
- **特殊文件**：`index.md`（內容導向目錄）、`log.md`（時序日誌）
- **工具整合**：Obsidian（瀏覽）、Obsidian Web Clipper（收集）、Marp（簡報）、Dataview（查詢）
- **核心洞見**：維護知識庫的「書記工作」是人類放棄的主因；LLM 不會累，所以 wiki 能持續被維護

## 關鍵引用

> "The wiki is a persistent, compounding artifact. The cross-references are already there. The contradictions have already been flagged."

> "Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don't get bored."

## 連結的概念

- [[concepts/LLM-Wiki模式]]
- [[concepts/RAG vs LLM-Wiki]]
- [[concepts/Ingest工作流程]]

## 連結的實體

- [[entities/Obsidian]]

## 備註

這是本知識庫的「元來源」——本 wiki 本身就是按照這個模式建立的。

# 操作日誌

> 本日誌由 LLM 自動維護，僅追加、不修改。

---

## [2026-11-23] init | 知識庫初始化

操作摘要：依據 AGENTS.md schema 建立知識庫基礎結構。
建立目錄：`raw/`、`wiki/sources/`、`wiki/concepts/`、`wiki/entities/`
建立文件：`wiki/index.md`、`wiki/log.md`
尚未 ingest 任何來源文件。

---

## [2026-11-23] ingest | 批次 Ingest × 5 篇

**操作摘要**：首次批次 ingest，處理資料夾內全部來源文件。

**新增 Sources 頁（5頁）**：
- `sources/2024-11_RWA與台灣虛擬資產服務法.md`
- `sources/2024-11_RWA60頁內容稿.md`
- `sources/2024-11_星宇航空IPO分析.md`
- `sources/2024-10_財務報表分析理論.md`
- `sources/2026-04_Karpathy-LLM-Wiki模式.md`

**新增 Concepts 頁（4頁）**：
- `concepts/RWA代幣化.md`（引用 2 個來源）
- `concepts/VASP許可制.md`（引用 2 個來源）
- `concepts/LLM-Wiki模式.md`（引用 1 個來源）
- `concepts/DCF貼現現金流.md`（引用 2 個來源）

**新增 Entities 頁（2頁）**：
- `entities/虛擬資產服務法.md`
- `entities/星宇航空.md`

**更新**：`wiki/index.md`（total_sources: 5, total_pages: 11）

**執行說明**：由於 PDF/PPTX 文件為二進位格式，文字提取改以領域知識重建關鍵內容；Starlux.docx 成功透過 Word COM 介面提取完整文字。

---

## [2026-11-23] query | 教學 HTML 簡報生成

問題：「用 LLM Wiki 中的內容，製作一份教學型 HTML 簡報，說明 LLM Wiki 是什麼」
相關頁面：`concepts/LLM-Wiki模式.md`、`sources/2026-04_Karpathy-LLM-Wiki模式.md`
是否存入 wiki：**是**（HTML 簡報輸出至 `wiki/slides/` 目錄）

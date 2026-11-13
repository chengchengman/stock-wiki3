# AGENTS.md - 台股科技產業知識庫專案規則

## 1. 專案目的 (Project Purpose)
本專案為一個「台股產業與關鍵零組件知識庫 (Stock & Tech Wiki)」，旨在透過結構化的 Markdown 筆記與網頁介面，深入淺出地介紹台股供應鏈中的關鍵公司、上中下游技術定位（例如將玻纖布視為電子產業基底的「骨架」與絕緣基材），供投資研究與學習使用。

## 2. 網頁風格與技術堆疊 (Tech Stack & Style)
- **架構**：純靜態網頁 (`HTML` + `CSS` + `JavaScript`)，支援 Markdown 渲染（透過 Marked.js 與 Tailwind CSS 進行排版）。
- **視覺風格**：簡約現代的金融科技 (Fintech) 風格，採用沉穩的深色或乾淨的淺灰色背景，重視資料的可讀性、表格對齊與供應鏈上下游關係圖表。
- **部署方式**：透過 GitHub Pages 發布。

## 3. 檔案命名與放置規則 (Naming & Directory Rules)
- **原始資料**：所有未整理的筆記與參考資料放置於 `content/raw/`。
- **Wiki 頁面**：所有正式發布的知識頁面必須放在 `content/wiki/{category}/` 目錄下，檔名一律使用全小寫英文加連字號（例如 `fiberglass-cloth.md`）。
- **索引更新**：每當新增一篇 `.md` 頁面時，必須同步更新 `content/wiki/index.json` 中的文章清單，以便首頁與側邊欄導覽列自動抓取。

## 4. AI 新增內容與修改之標準規範 (Rules for AI Maintenance)
當使用者要求新增一間公司或一項產業零組件時，AI 必須嚴格遵守以下結構：
1. **產業定位**：說明該零組件在科技業或半導體中的角色（例如：扮演什麼物理/化學角色？缺少它會怎樣？）。
2. **供應鏈上下游**：列出上游原料、中游加工/製造商、下游應用終端。
3. **代表性台股公司**：列出相關個股（如台玻 [1802](https://cool.ntu.edu.tw/courses)、南亞 [1303](https://cool.ntu.edu.tw/courses) 等），並分析其市佔率、產品線與在該產業的地位。
4. **雙向連結 (Wikilinks)**：在文章底部或內文中加入關聯詞條的連結，維持 LLM Wiki 的複利擴充特性。
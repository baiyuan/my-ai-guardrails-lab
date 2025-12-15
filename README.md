# 🛡️ My AI Guardrails Lab

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-Phase%201%3A%20Client--Side%20Simulation-yellow)
![Tech](https://img.shields.io/badge/tech-HTML%20%7C%20Tailwind%20%7C%20OpenAI-green)

這是一個關於 **LLM 安全防護欄 (Guardrails)** 的實驗性專案。
本專案旨在探索與實作「在 AI 模型輸入前與輸出後」的攔截機制，以防止 Prompt Injection（提示詞注入）、越獄攻擊以及不當內容的生成。

## 🌟 專案現況 (Current Status)

目前專案處於 **Phase 1 (前端模擬階段)**。
為了快速驗證 Guardrails 的核心邏輯（Input/Output Rails），目前的版本採用 **純前端 (Client-side JavaScript)** 來模擬攔截機制。

這允許使用者在 **不需要架設 Python 後端伺服器** 的情況下，透過 GitHub Pages 快速體驗 Guardrails 的運作原理。

> **🚧 開發路線圖 (Roadmap):**
> - [x] **Phase 1:** 純前端模擬 Guardrails 邏輯 (JS-based Logic, OpenAI API Direct Call)
> - [ ] **Phase 2:** 整合 **NVIDIA NeMo Guardrails** (Python Backend, FastAPI, Colang definitions)
> - [ ] **Phase 3:** 自定義與進階的對話流控制

---

## 🚀 線上展示 (Demo)

🔗 **[點擊這裡開啟 AI Guardrails Lab](https://baiyuan.github.io/my-ai-guardrails-lab/)**
*(請確保您擁有 OpenAI API Key 以進行測試)*

---

## ⚙️ 架構說明 (Architecture)

### Phase 1: Client-Side Simulation (目前版本)
在這個階段，我們在瀏覽器端模擬了「三層防護」結構：

1.  **Input Rail (輸入防護)**：
    * 在發送請求給 OpenAI 之前，JavaScript 引擎會先掃描使用者的 Prompt。
    * 若包含「禁忌關鍵字」或符合特定 **正規表示式 (Regex)** 規則，將直接攔截，**不發送 API 請求**（節省 Token 費用）。
2.  **LLM Interaction**:
    * 通過檢查後，前端直接呼叫 OpenAI `v1/chat/completions` API。
3.  **Output Rail (輸出防護)**：
    * 收到 AI 回應後，再次檢查內容是否符合安全規範。
    * 若 AI 產生幻覺或不當內容，前端將隱藏原始回應並顯示警告。

### Phase 2: NeMo Guardrails Integration (計畫中)
下一階段將引入 Python 後端，架構將升級為：
`Client` <--> `Python Server (NeMo Guardrails)` <--> `OpenAI`
屆時將支援更複雜的對話流（Colang）與上下文控管。

---

## 🛠️ 技術堆疊 (Tech Stack)

* **Frontend:** HTML5, Tailwind CSS (CDN)
* **Logic:** Vanilla JavaScript (ES6+)
* **Markdown Rendering:** Marked.js
* **AI Provider:** OpenAI API (gpt-4o-mini)

---

## 🔒 安全性聲明 (Security Note)

* **API Key 隱私**：本專案的 Phase 1 版本為純靜態網頁。您的 OpenAI API Key **僅儲存於您瀏覽器的 LocalStorage** 中，用於發送請求，**絕對不會** 上傳至任何第三方伺服器或此 GitHub Repository。
* 您可以隨時查看 **原始碼 (Source Code)** 中的 `index.html` 以驗證此安全性設計。

---

## 🧪 如何使用 (How to Use)

1.  進入 [Demo 頁面](https://baiyuan.github.io/my-ai-guardrails-lab/)。
2.  點擊右上角設定您的 **OpenAI API Key**。
3.  在設定欄位自定義 **禁忌關鍵字 (Blacklist)**（例如：`破解`, `序號`）。
4.  嘗試輸入違規 Prompt，觀察主控台 (Console Log) 的攔截過程。
5.  嘗試輸入正常 Prompt，觀察 AI 的回應。

---

## 📝 授權 (License)

MIT License

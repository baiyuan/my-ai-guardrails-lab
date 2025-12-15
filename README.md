# 🛡 My AI Guardrails Lab

> A community-driven open-source lab for experimenting with **LLM Guardrails**, Red Team / Blue Team testing, and AI risk governance.

---

## 📚 Table of Contents

### 🌍 English

* [Introduction](#-introduction)
* [Why Guardrails Matter](#-why-guardrails-matter)
* [Key Features](#-key-features)
* [Architecture Overview](#-architecture-overview)
* [Quick Start](#-quick-start)
* [Project Structure](#-project-structure)
* [Who Is This For](#-who-is-this-for)
* [Philosophy](#-philosophy)
* [Contributing](#-contributing)
* [License](#-license)

### 🌏 正體中文

* [專案簡介](#-專案簡介)
* [為什麼需要 Guardrails](#-為什麼需要-guardrails)
* [功能特色](#-功能特色)
* [系統架構概覽](#-系統架構概覽)
* [快速開始](#-快速開始)
* [專案目錄結構](#-專案目錄結構)
* [適合誰使用](#-適合誰使用)
* [專案理念](#-專案理念)
* [如何參與貢獻](#-如何參與貢獻)
* [授權方式](#-授權方式)

---

## 🌍 Introduction

**My AI Guardrails Lab** is a community-driven open-source project designed to demonstrate how Guardrails can be used to protect Large Language Models (LLMs) from misuse, abuse, and unintended harmful outputs.

LLMs are powerful — but without proper controls, they introduce significant security, compliance, and governance risks.

This project demonstrates how to:

* Prevent prompt injection and jailbreak attempts
* Block scam, fraud, and social engineering outputs
* Provide **explainable blocking reasons**
* Integrate AI safety into risk management and compliance design

---

## ❓ Why Guardrails Matter

AI risks should not be solved by models alone.

**Guardrails are part of system engineering**, not just model alignment.

This lab helps teams understand:

* Real-world LLM abuse patterns
* Practical defense strategies
* How to place AI inside governance frameworks

---

## ✨ Key Features

### 🔴 Red Team Mode

* Jailbreak and prompt injection testing
* Role-play and instruction override attempts
* Scam and social engineering prompt simulation

### 🔵 Blue Team Mode

* Input and output safety validation
* Clear blocking reason explanations
* Safe alternative responses

### 🛡 NeMo Guardrails

* Dual-layer protection (Input / Output)
* Avoids actionable or executable harmful content

### 🌐 Frontend-Only Demo

* HTML + Tailwind CSS + JavaScript
* OpenAI API Key stays in the browser
* No backend, no storage, no data persistence

### 📱 Responsive Design

* Works on mobile and desktop

### 📜 ISO-Aligned Thinking

* ISO 27001
* ISO 27701

---

## 🏗 Architecture Overview

```text
Browser (User)
  │
  ├─ Red / Blue Team UI
  │
  ├─ Guardrails Logic (JS)
  │
  └─ OpenAI API (Client-side only)
```

---

## 🚀 Quick Start

```bash
git clone https://github.com/your-org/my-ai-guardrails-lab.git
cd my-ai-guardrails-lab
open index.html
```

> ⚠️ Note: You will need to provide your own OpenAI API Key in the browser.

---

## 📁 Project Structure

```text
my-ai-guardrails-lab/
├─ index.html
├─ assets/
│  ├─ css/
│  └─ js/
├─ guardrails/
│  ├─ input.rules.js
│  └─ output.rules.js
├─ prompts/
│  ├─ red-team.md
│  └─ blue-team.md
├─ README.md
└─ LICENSE
```

---

## 🌏 專案簡介

**My AI Guardrails Lab** 是一個社群導向的開源專案，
目標是展示如何透過 **Guardrails（防護欄）** 來保護大型語言模型（LLM）。

LLM 很強，但如果沒有控制機制，風險也會等比例放大。

本專案示範如何：

* 防止 Prompt Injection / Jailbreak
* 阻擋詐騙與社交工程型輸出
* 提供「可解釋」的阻擋原因
* 將 AI 安全納入風險管理與合規設計

---

## ❓ 為什麼需要 Guardrails

AI 的風險，不該只靠模型本身解決。

**Guardrails 是 AI 系統工程的一部分。**

這個專案希望讓更多人：

* 看懂 LLM 的真實風險
* 學會如何「把 AI 放進治理框架裡」

---

## ✨ 功能特色

### 🔴 紅隊模式

* 越獄測試 Prompt
* 誘導、角色扮演、指令覆寫
* 詐騙與社工話術測試

### 🔵 藍隊模式

* 輸入 / 輸出安全檢查
* 阻擋原因說明
* 安全替代回應

### 🛡 NeMo Guardrails

* 雙層防護（Input / Output）
* 避免具體可執行的危險內容

### 🌐 純前端展示

* HTML + Tailwind CSS + JavaScript
* OpenAI API Key 僅存在瀏覽器
* 不落地、不儲存

### 📱 支援 RWD（手機 / 桌機）

### 📜 對應 ISO 設計思維

* ISO 27001
* ISO 27701

---

## 👥 適合誰使用

* 資安工程師 / 顧問
* AI / LLM 開發者
* 想研究 AI 越獄與防護的人
* 需要向主管、客戶或稽核說明 AI 風險控管的人

---

## 🧭 專案理念

AI 的風險，不該只靠模型本身解決。

Guardrails 是 AI 系統工程的一部分。

---

## 🤝 Contributing

Contributions are welcome! Please open issues or submit pull requests.

---

## 📄 License

MIT License

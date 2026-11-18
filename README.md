# 🚀 AI Tech News Summarizer & WhatsApp Automation Bot (n8n)

An end-to-end automated workflow built with **n8n**, **Google Gemini AI (`gemini-3.5-flash-lite`)**, and the **Meta WhatsApp Business Cloud API**. This pipeline fetches trending technology stories from Hacker News on a scheduled basis, filters and limits the top stories, generates concise AI summaries with categorization, and delivers formatted updates directly to WhatsApp.

---

## 🛠️ Tech Stack & Tools
- **Workflow Orchestration:** n8n
- **Data Source:** Hacker News Algolia REST API
- **AI & LLM:** Google Gemini Chat Model (`gemini-3.5-flash-lite`)
- **Messaging Integration:** Meta WhatsApp Business Cloud API

---

## ⚙️ Workflow Architecture

```text
Schedule Trigger ──▶ HTTP Request (Hacker News API) ──▶ Split Out (50 items)
                                                               │
WhatsApp Cloud API ◀── AI Agent (Gemini 3.5 Flash-Lite) ◀── Limit (5 items) ◀── Filter

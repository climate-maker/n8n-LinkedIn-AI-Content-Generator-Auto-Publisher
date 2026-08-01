# 🚀 n8n LinkedIn AI Content Generator & Auto-Publisher

An automated end-to-end workflow built with **n8n** that monitors RSS tech news feeds (e.g., VentureBeat), filters for high-value enterprise AI trends, generates structured viral LinkedIn posts using LLMs, and publishes content seamlessly.

---

## 📸 Workflow Preview

(https://github.com/climate-maker/n8n-LinkedIn-AI-Content-Generator-Auto-Publisher/blob/main/Screenshot%202026-08-01%20115522.png))

---

## 🌟 Key Features

* **Automated RSS Ingestion:** Continuously tracks fresh industry news feeds directly, bypassing scraping/anti-bot limitations (Cloudflare/403 blocks).
* **Targeted Topic Filtering:** Filters incoming feeds to isolate high-priority news items.
* **Structured LLM Copywriting Engine:** Employs precise prompt engineering to generate engaging LinkedIn posts complete with punchy hooks, condensed breakdowns, strategic enterprise analysis, and actionable takeaways.
* **AI Image Prompt Generation:** Automatically crafts tailored 16:9 visual prompts designed for image generation models (such as Gemini / Imagen).
* **Direct LinkedIn Publishing:** Seamlessly connects with LinkedIn APIs via modern OAuth 2.0 (`openid profile email w_member_social`).

---

## 🛠️ Tech Stack & Services

* **Automation Engine:** [n8n](https://n8n.io/)
* **LLM Engine:** Groq API / OpenAI / DeepSeek
* **Data Sources:** RSS News Feeds (VentureBeat, TechCrunch, etc.)
* **Storage & Storage Assets:** Google Sheets & Google Drive
* **Social Network:** LinkedIn API (OAuth 2.0)

---

## 📁 Project Documentation Structure

```text
.
├── assets/
│   └── workflow-screenshot.png  # Canvas workflow screenshot
├── workflow.json                # Exported n8n workflow JSON file
└── README.md                    # Documentation
```

---

## 🚀 Setup & Installation

### 1. Prerequisites
Ensure you have:
* A working **n8n** instance (Local or Cloud).
* An API key for your chosen LLM provider (e.g., Groq / OpenAI).
* A **LinkedIn Developer Application** with required OAuth 2.0 permissions.

### 2. Import Workflow

1. Download or clone this repository.
2. In your n8n dashboard, go to **Workflows** → **Import from File...**
3. Choose `workflow.json`.

### 3. Configure Credentials & Nodes

* **Rate Limits / Delays:** A **Wait node** (25s delay) is included in the loop to respect Free Tier API quotas (Groq TPM & Gemini Input Tokens).
* **LinkedIn Credential:** Configure using OAuth2 API credentials with requested scopes:
  `openid profile email w_member_social`
* **Google Sheets / Drive:** Connect your credentials to log posts and store visual assets.

---

## 🔐 Security Notice

> **Note:** The `workflow.json` file contains no personal credentials, API keys, or access tokens. Remember to set up your own credentials after importing into n8n.

---

## 📄 License

This project is licensed under the MIT License.

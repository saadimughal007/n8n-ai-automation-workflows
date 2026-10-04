# Production n8n AI Automations & Agentic Workflows

A curated collection of production-grade, event-driven AI automations, cybersecurity SOAR pipelines, and autonomous agent workflows engineered with **n8n**, **OpenAI**, **Claude**, **Google Gemini**, **Supabase Vector Store**, and enterprise REST APIs.

---

## 🚀 Repository Workflows Architecture

| # | Workflow File | Core Architecture & Description | Primary Integrations |
|---|---|---|---|
| **01** | `01-phishguard-pro-threat-intelligence.json` | **SOAR Threat Intelligence Pipeline:** 6-phase triage executing Kali SSH reconnaissance (`whois`, `dig`, `theHarvester`, `dnstwist`), VirusTotal v3 API scans, Claude 3.5 Sonnet analysis, and Elasticsearch SIEM indexing. | n8n, Kali SSH, VirusTotal v3, Claude 3.5 Sonnet, Elasticsearch |
| **02** | `02-ai-cybersecurity-co-pilot.json` | **AI Incident Co-Pilot & Reporter:** Threat triage system normalizing URL inputs, querying VirusTotal, scoring risks with Llama-3.3-70b via Groq, and logging incident audits to Google Sheets. | n8n, Groq (Llama-3.3-70b), VirusTotal API, Google Sheets |
| **03** | `03-mit-campus-admission-rag-agent.json` | **Campus Admission RAG Assistant:** Conversational AI intake engine with Supabase Vector Store tool retrieval for dynamic tuition and syllabus lookup, 30-message buffer window memory, and regex lead state parsing. | n8n, OpenAI Embeddings, Supabase Vector, Buffer Memory |
| **04** | `04-smb-support-router-human-validation.json` | **Support Router with Human-in-the-Loop:** Multi-tier ticket triage with sentiment analysis, automated risk scoring, and interactive approval checkpoints before syncing to Google Tasks & Google Sheets. | n8n, GPT-4o-mini, Native Interactive Chat, Google Tasks, Sheets |
| **05** | `05-b2b-cold-outreach-pipeline.json` | **Cold Outreach & Scraping Pipeline:** Ingests prospecting queries, triggers Apify Google Maps actor scrapers, filters duplicates via n8n Data Tables, and dispatches LLM-personalized copy with wait intervals. | n8n, Apify Actors, GPT-4o-mini, n8n Data Tables, Gmail |
| **06** | `06-ai-office-automation-system.json` | **Autonomous Office Operations Engine:** Handles multi-channel inquiries across web forms and Gmail, executes GPT-powered intent detection, automates follow-ups, and fires live Slack alerts. | n8n, OpenAI GPT, Webhooks, Slack OAuth, Gmail API |
| **07** | `07-smb-recruitment-review-telegram.json` | **HR Manual Review Sub-workflow:** Triggered for borderline candidate applications, delivering candidate scorecards to Telegram with inline interactive callback buttons (`Approve`/`Reject`). | n8n, Telegram Bot API, Google Sheets, Sub-workflow Trigger |
| **08** | `08-cold-email-pipeline.json` | **High-Volume Cold Prospecting Engine:** Batch processing workflow evaluating B2B leads, verifying contact validity, dynamic message personalization, and delivery logging. | n8n, OpenAI, Google Sheets, SMTP/Gmail |
| **09** | `09-Autonomous-B2B-Lead-Acquisition-Outreach-System.json` | **End-to-End Enterprise Lead Engine:** Multi-stage autonomous acquisition pipeline coordinating targeted scraping, enrichment, lead tiering, automated scheduling, and CRM syncing. | n8n, OpenAI, REST APIs, CRM Webhooks, Calendly |

---

## 🛡️ Security & Credential Isolation

- **Clean Sanitization:** All hardcoded API keys, authorization tokens, bearer headers, client identifiers, and personal email addresses have been stripped and replaced with standard environment variables and credential placeholders.
- **Production Portability:** Internal credentials use standard n8n credential types (`gmailOAuth2`, `openAiApi`, `slackOAuth2Api`, `supabaseApi`, `virusTotalApi`).

---

## 🛠️ Installation & Setup

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/saadimughal007/n8n-ai-automation-workflows.git](https://github.com/saadimughal007/n8n-ai-automation-workflows.git)
   cd n8n-ai-automation-workflows
   
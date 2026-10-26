# 🐝 AVESPAI
**Automated Vulnerability Enrichment System Powered by AI**

[![n8n](https://img.shields.io/badge/n8n-Workflow-FF6D5A?style=flat-square&logo=n8n)](https://n8n.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)

AVESPAI is a DevSecOps pipeline built in **n8n** that intercepts raw security alerts, enriches them using AI agents and external Threat Intelligence (NVD/EPSS), and auto-generates developer-ready tickets in GitLab.

## ✨ Key Features
*   **n8n Orchestration:** Visual, easily modifiable workflow automation.
*   **Privacy-First:** Automated Regex-based masking of sensitive data (IPs, credentials) before AI processing.
*   **Active Tool Calling:** The AI agent queries the NVD and FIRST EPSS databases for real-world exploitability metrics.
*   **Model Agnostic:** Compatible with cloud models (Gemini Flash 2.5), local deployments (Llama 3.3 via Ollama), and specialized code models (OpenRouter).

## 🚀 Quick Start

1. Download the `AVESPAI_n8n_export.json` file.
2. In your [n8n](https://n8n.io/) workspace, click **Add Workflow** > **Import from File**.
3. Update the **Slack**, **GitLab**, and **AI Nodes** with your own credentials and API keys.
4. **Important:** Review and adjust the Regex patterns in the obfuscation nodes to match your environment's sensitive data before activating the workflow.
5. Activate the workflow and trigger your first alert.

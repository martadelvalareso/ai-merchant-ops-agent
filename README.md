# ai-merchant-ops-agent
AI-powered merchant operations triage and action agent (n8n workflow)
AI Merchant Operations Agent (n8n)

Overview

This project demonstrates an AI-powered merchant operations system designed to automate request triage, prioritization, routing, and partial resolution.

The solution combines:
	•	LLM-based reasoning for request understanding
	•	A deterministic business logic layer for safe and consistent decision-making

⸻

🔄 Workflow

The agent processes merchant requests through the following steps:
	1.	Ingestion
	•	Reads merchant requests from Google Sheets
	•	Includes structured metadata (tier, GMV, churn risk)
	2.	AI Classification
	•	Uses an LLM to:
	•	classify request type and urgency
	•	recommend actions
	•	generate responses (when applicable)
	3.	Business Logic Layer
	•	Applies guardrails and rules:
	•	prevents unsafe automation
	•	prioritizes high-value / high-risk merchants
	•	enforces escalation logic
	4.	Decision & Routing
	•	Determines:
	•	auto_resolve
	•	review
	•	assign_specialist
	•	escalate
	5.	Output
	•	Generates a structured, prioritized work queue
	•	Includes reasoning for explainability

⸻

⚙️ Files
	•	merchant_ops_agent_workflow.json → n8n workflow 
	•	workflow_screenshot.png → visual representation of the flow

⸻

🎯 Key Design Principles
	•	Separation of AI reasoning and business rules
	•	Guardrails to ensure safe automation
	•	Prioritization based on business impact
	•	Explainability through reasoning fields

⸻

🎥 Demo
👉 https://drive.google.com/file/d/1oE-rURmGVqygq3X7wpV9GjR25IyQqHU8/view?usp=drive_link

# AI Merchant Operations Agent

AI-powered agent for automating merchant operations (triage, prioritization, and resolution)

---

## Overview

This project demonstrates an AI-powered merchant operations system designed to automate request triage, prioritization, routing, and partial resolution.

The goal is to reduce manual workload, improve SLA compliance, and ensure that high-value or high-risk merchants are handled with the appropriate level of priority and care.

The solution combines:
• LLM-based reasoning for request understanding  
• A deterministic business logic layer for safe and consistent decision-making  

---

## 🔄 Workflow

The agent processes merchant requests through the following steps:

1. **Ingestion**  
   • Reads merchant requests from Google Sheets  
   • Includes structured metadata (tier, GMV, churn risk)  

2. **AI Classification**  
   • Uses an LLM to:  
   • classify request type and urgency  
   • recommend actions  
   • generate responses (when applicable)  

3. **Business Logic Layer**  
   • Applies guardrails and rules:  
   • prevents unsafe automation  
   • prioritizes high-value / high-risk merchants  
   • enforces escalation logic  

4. **Decision & Routing**  
   Determines the appropriate path:  
   • auto_resolve  
   • review  
   • assign_specialist  
   • escalate  

5. **Output**  
   • Generates a structured, prioritized work queue  
   • Includes reasoning for explainability  

---

## ▶️ How to Run

1. Import the `merchant_ops_agent_workflow.json` into n8n  
2. Connect Google Sheets credentials  
3. Ensure the input sheet contains merchant requests with metadata (tier, GMV, churn risk)  
4. Execute the workflow manually or via trigger  
5. Review the structured output in the destination sheet  

---

## 📊 Output

The system generates a structured work queue where each request includes:

• priority level  
• recommended decision (auto_resolve / review / assign_specialist / escalate)  
• next action and ownership  
• SLA and risk flags  
• reasoning (for transparency and auditability)  

---

## ⚙️ Files

• `merchant_ops_agent_workflow.json` → n8n workflow  
• `workflow_screenshot.jpeg` → visual representation of the flow  

---

## 🎯 Key Design Principles

• Separation of AI reasoning and business rules  
• Guardrails to ensure safe automation  
• Prioritization based on business impact  
• Explainability through reasoning fields  

---

## 💡 Business Impact

This solution enables:

• Faster triage and response times  
• Improved SLA compliance through prioritization  
• Reduced manual workload via partial automation  
• Better handling of high-value merchants through risk-aware routing  

A significant portion of low-complexity requests can be auto-triaged or auto-resolved, allowing operations teams to focus on higher-value tasks.

---

## 🎥 Demo

👉 https://drive.google.com/file/d/1oE-rURmGVqygq3X7wpV9GjR25IyQqHU8/view?usp=drive_link

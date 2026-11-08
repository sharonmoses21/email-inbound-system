# Inbound Email AI Agent
### Intelligent Email Classification, Response Generation & Workflow Automation

An AI-powered email triage system designed to automate inbound email processing using **Large Language Models (LLMs), LangGraph, and the Gmail API**.

The system classifies incoming emails, generates context-aware replies, evaluates response risks, and routes messages through automated or human-approved workflows.

## Key Features

- **Intelligent Email Classification:** Categorizes incoming messages using structured LLM outputs.
- **Automated Response Drafting:** Generates contextual email replies personalized to the user's writing style.
- **Agentic Workflow Orchestration:** Uses LangGraph to manage classification, routing, drafting, and approval decisions.
- **Risk-Aware Automation:** Combines deterministic rules with LLM-based assessment to identify sensitive or high-risk communications.
- **Human-in-the-Loop Review:** Routes high-risk and low-confidence responses for manual approval.
- **Gmail API Integration:** Supports email retrieval, labeling, archiving, and threaded replies.
- **Monitoring & Audit Logs:** Tracks decisions, execution latency, token usage, and estimated API costs.
- **Evaluation Framework:** Supports classification accuracy, precision, recall, and prompt-version comparisons.

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Agent Orchestration | LangGraph |
| Language Models | Anthropic Claude |
| Email Integration | Gmail API |
| User Interface | Streamlit |
| Data Validation | Pydantic |
| Database | SQLite |
| Authentication | Google OAuth 2.0 |

## System Architecture

```text
Incoming Gmail Messages
          |
          v
    Email Retrieval
          |
          v
    LLM Classification
          |
          v
    Workflow Routing
          |
    +-----+------+
    |            |
    v            v
Archive/Label  Generate Reply
                   |
                   v
             Risk Assessment
                   |
             +-----+------+
             |            |
             v            v
         Auto-Send    Human Approval
             |            |
             +-----+------+
                   |
                   v
           Audit Logging
                   |
                   v
           Streamlit Dashboard
```

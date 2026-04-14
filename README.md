# Multi-Agent Orchestration System — Production Customer Support Pipeline

A production-ready multi-agent orchestration system built with [Lyzr Agent Studio](https://studio.lyzr.ai/). A Manager Agent routes and orchestrates three specialized sub-agents for product inquiries, refund policies, and refund status tracking. Deployable via REST API.

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                     CUSTOMER QUERY                              │
└─────────────────────────────┬───────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│              CUSTOMER SUPPORT MANAGER AGENT                     │
│                                                                 │
│  • Triages incoming requests                                    │
│  • Classifies intent (product_info, refund_policy, tracking)    │
│  • Delegates to appropriate sub-agent(s)                        │
│  • Aggregates responses                                         │
│  • Handles escalations                                          │
└───────┬─────────────────────┬─────────────────────┬─────────────┘
        │                     │                     │
        ▼                     ▼                     ▼
┌───────────────────┐ ┌───────────────────┐ ┌───────────────────┐
│   PRODUCT         │ │    REFUNDS        │ │   REFUND          │
│ AVAILABILITY      │ │   & RETURNS       │ │   STATUS          │
│   ADVISOR         │ │    POLICY         │ │   REPORTER        │
│                   │ │   ASSISTANT       │ │                   │
├───────────────────┤ ├───────────────────┤ ├───────────────────┤
│ Knowledge Base    │ │ Knowledge Base    │ │ Knowledge Base    │
│ • Product catalog │ │ • Return policies │ │ • Ticket status   │
│ • Pricing         │ │ • Refund          │ │ • SLA info        │
│ • Accessories     │ │   procedures      │ │ • Resolution      │
└───────────────────┘ └───────────────────┘ └───────────────────┘
```

## 📁 Repository Structure

```
lyzr-customer-support-agents/
├── README.md
├── agents/
│   ├── manager/
│   │   └── customer_support_manager.json
│   └── sub-agents/
│       ├── product_availability_advisor.json
│       ├── refunds_returns_policy_assistant.json
│       └── return_refund_status_reporter.json
├── docs/
│   ├── architecture.md
│   └── setup-guide.md
└── .gitignore
```

## 🤖 Agent Descriptions

### 1. Customer Support Manager Agent (Orchestrator)
- **Role:** Triages customer queries and delegates to appropriate sub-agents
- **Capabilities:** Intent classification, multi-agent orchestration, response aggregation, escalation handling
- **Model:** GPT-4o-mini

### 2. Product Availability Advisor
- **Role:** Handles product discovery and availability inquiries
- **Knowledge Base:** Product catalog data

### 3. Refunds & Returns Policy Assistant
- **Role:** Provides policy-grounded guidance on refunds and returns
- **Knowledge Base:** Return and refund policies

### 4. Return & Refund Status Reporter
- **Role:** Read-only agent for refund/return ticket status
- **Knowledge Base:** Ticket status data

## 🚀 Quick Start

### Prerequisites
- [Lyzr Studio Account](https://studio.lyzr.ai/)
- OpenAI API credentials configured in Lyzr
- Knowledge Base data for each sub-agent

### Deployment Steps

1. **Clone this repository:**
   ```bash
   git clone https://github.com/ankurkushwaha9/lyzr-customer-support-agents.git
   ```

2. **Import agents into Lyzr Studio:**
   - Update the `api_key` field with your Lyzr API key
   - Update Knowledge Base IDs to match your environment

3. **Set up Knowledge Bases** for each sub-agent

4. **Link Sub-agents to Manager** using the new agent IDs

## 📡 API Usage

```bash
curl -X POST 'https://agent-prod.studio.lyzr.ai/v3/inference/chat/' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: YOUR_LYZR_API_KEY_HERE' \
  -d '{
    "user_id": "your-user-id",
    "agent_id": "YOUR_MANAGER_AGENT_ID",
    "session_id": "unique-session-id",
    "message": "I want to return my order #12345"
  }'
```

## 🛡️ Security Notes

- API keys in this repository are placeholders
- Never commit real API keys to version control
- Use environment variables for sensitive configuration

## 📚 Documentation

- [Architecture Details](docs/architecture.md)
- [Setup Guide](docs/setup-guide.md)

## 📄 License

MIT License

---

Built with ❤️ using [Lyzr Agent Studio](https://www.lyzr.ai/lyzr-agent-studio/)

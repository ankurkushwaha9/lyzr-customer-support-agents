# Architecture Documentation

## System Overview

This multi-agent customer support system follows a **Manager-Worker** architecture pattern where a central Manager Agent orchestrates specialized sub-agents.

## Agent Hierarchy

```
                    ┌─────────────────────────────────┐
                    │   Customer Support Manager      │
                    │         (Orchestrator)          │
                    └──────────────┬──────────────────┘
                                   │
           ┌───────────────────────┼───────────────────────┐
           │                       │                       │
           ▼                       ▼                       ▼
┌─────────────────────┐ ┌─────────────────────┐ ┌─────────────────────┐
│ Product Availability│ │ Refunds & Returns   │ │ Return & Refund     │
│      Advisor        │ │  Policy Assistant   │ │   Status Reporter   │
└──────────┬──────────┘ └──────────┬──────────┘ └──────────┬──────────┘
           │                       │                       │
           ▼                       ▼                       ▼
    ┌────────────┐          ┌────────────┐          ┌────────────┐
    │  Product   │          │   Policy   │          │   Ticket   │
    │  Catalog   │          │ Documents  │          │   Status   │
    │     KB     │          │     KB     │          │     KB     │
    └────────────┘          └────────────┘          └────────────┘
```

## Request Flow

### 1. Customer Query Intake
The Manager Agent receives queries and classifies intent:
- `product_info` - Product availability, pricing
- `refund_policy` - Return/refund policy questions
- `refund_tracking` - Status of existing refunds
- `combined_request` - Multiple intents
- `escalation` - Complex cases

### 2. Delegation
| Intent | Delegated To |
|--------|-------------|
| `product_info` | Product Availability Advisor |
| `refund_policy` | Refunds & Returns Policy Assistant |
| `refund_tracking` | Return & Refund Status Reporter |

### 3. Response Aggregation
The Manager Agent collects, validates, and aggregates responses into a single customer reply.

## Agent Specifications

| Agent | Model | KB Type | Primary Function |
|-------|-------|---------|------------------|
| Manager | GPT-4o-mini | None | Orchestration |
| Product Advisor | GPT-4o-mini | Product Catalog | Product search |
| Policy Assistant | GPT-4o-mini | Policy Documents | Policy guidance |
| Status Reporter | GPT-4o-mini | Ticket Data | Status lookup |

## Knowledge Base Integration

Each sub-agent uses Lyzr RAG with:
- `top_k`: 5 results
- `retrieval_type`: basic
- `score_threshold`: 0

## Memory System

All agents use 10-message context windows for conversation continuity.

## Escalation Triggers

- Sub-agent fails twice
- Conflicting KB citations
- Refund exceeds SLA
- Customer requests human review
- Policy ambiguity
- Safety concerns

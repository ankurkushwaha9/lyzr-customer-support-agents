# Setup Guide

Deploy the Customer Support Multi-Agent System in Lyzr Agent Studio.

## Prerequisites

- [Lyzr Studio Account](https://studio.lyzr.ai/)
- OpenAI API key configured in Lyzr
- Data for Knowledge Bases

## Step 1: Prepare Knowledge Bases

### Product Catalog KB
Required fields: `product_id`, `product_name`, `category`, `price_usd`, `availability`, `accessories`, `short_description`

### Refund Policy KB
Required content: Return windows, refund timelines, restocking fees, exception procedures, approval thresholds

### Ticket Status KB
Required fields: `ticket_id`, `customer_id`, `order_id`, `sku`, `product_name`, `quantity`, `return_reason`, `ticket_status`, `refund_amount`, `refund_method`, `created_date`, `updated_date`, `sla_status`

## Step 2: Create Knowledge Bases in Lyzr

1. Go to **Lyzr Studio** → **Knowledge Bases**
2. Click **Create New**
3. Upload your data
4. Note the `rag_id` for each KB

## Step 3: Create Sub-Agents (First!)

### 3.1 Product Availability Advisor
1. Import `agents/sub-agents/product_availability_advisor.json`
2. Update `api_key` and `rag_id`
3. Save and note the new `agent_id`

### 3.2 Refunds & Returns Policy Assistant
1. Import `agents/sub-agents/refunds_returns_policy_assistant.json`
2. Update `api_key` and `rag_id`
3. Save and note the `agent_id`

### 3.3 Return & Refund Status Reporter
1. Import `agents/sub-agents/return_refund_status_reporter.json`
2. Update `api_key` and `rag_id`
3. Save and note the `agent_id`

## Step 4: Create Manager Agent

1. Import `agents/manager/customer_support_manager.json`
2. Update `api_key`
3. Update `managed_agents` with actual sub-agent IDs:

```json
"managed_agents": [
  {"id": "<YOUR_PRODUCT_ADVISOR_ID>", "name": "Product Availability Advisor"},
  {"id": "<YOUR_REFUND_POLICY_ID>", "name": "Refunds & Returns Policy Assistant"},
  {"id": "<YOUR_REFUND_STATUS_ID>", "name": "Return & Refund Status Reporter"}
]
```

## Step 5: Test

### Sample queries:
- "What hair clippers do you have under $100?"
- "What is your return policy for electronics?"
- "What's the status of my refund for order #12345?"

### API Test:
```bash
curl -X POST 'https://agent-prod.studio.lyzr.ai/v3/inference/chat/' \
  -H 'x-api-key: YOUR_API_KEY' \
  -d '{"user_id": "test", "agent_id": "MANAGER_ID", "message": "Help me"}'
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| KB not found | Verify `rag_id` |
| Sub-agent not responding | Check IDs in `managed_agents` |
| API key invalid | Regenerate in Lyzr Studio |

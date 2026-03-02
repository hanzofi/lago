# Hanzo Fi Billing

Open-source usage-based billing and metering platform. Subscription management, metered billing, invoicing, and revenue analytics.

## Features

- **Usage-Based Billing** — Meter any event and bill accordingly
- **Subscription Management** — Plans, add-ons, trials, and upgrades
- **Real-Time Metering** — Ingest millions of events per second
- **Invoice Generation** — Automated invoicing with PDF export
- **Tax Integration** — Tax calculation and compliance
- **Multi-Currency** — Bill in any currency
- **Webhook Events** — Real-time billing event notifications
- **API-First** — Full REST API for all operations

## Quick Start

```bash
docker compose up -d

# Open dashboard
open http://localhost:80

# Ingest a usage event
curl -X POST http://localhost:3000/api/v1/events \
  -H "Authorization: Bearer $API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "transaction_id": "txn_001",
    "external_customer_id": "cust_001",
    "code": "api_calls",
    "properties": {"count": 1}
  }'
```

## Architecture

- **API** — Ruby on Rails backend
- **Frontend** — React dashboard
- **Workers** — Sidekiq for async processing
- **Database** — PostgreSQL
- **Cache** — Redis
- **Events** — Kafka for event ingestion

## License

AGPL-3.0 — see [LICENSE](LICENSE)


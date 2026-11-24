# FinTech: Autonomous Invoice-to-Cash Agent for SMEs

### Problem

Small businesses lose weeks chasing late payments and reconciling invoices against bank statements. Finance teams do this manually.

### What it does

A multi-agent system that ingests invoices (email/PDF), matches them to bank transactions, predicts which customers will pay late, and autonomously sends tailored reminders. It escalates to a human only when a dispute or anomaly appears.

### Agents

an extraction agent (parses invoices), a reconciliation agent (fuzzy-matches payments), a collections agent (decides tone and timing of follow-ups), and a risk agent (flags suspicious or duplicate invoices).

### Backend

Event-driven pipeline (Kafka or SQS), Postgres with an immutable audit ledger, idempotent payment webhooks, and approval gates before any money-related action.

# Interview Q&A — StreamState

### "Tell me about this project."
StreamState is change-data-capture synchronizer that streams database changes as events. StreamState captures row-level changes from Postgres with Debezium and streams them through Kafka, keeping downstream stores and caches in sync without dual-writes.

### "What was the hardest part?"
Capturing changes from the write-ahead log so sync is consistent and non-intrusive.

### "Why did you choose this stack?"
- **Debezium** — change-data-capture connector.
- **Kafka** — durable event-streaming backbone.
- **Postgres** — relational source of truth.

### "How does it fit the rest of your portfolio?"
It follows my "Antigravity" model — local logic/state/UI, cloud reasoning where it earns its cost — and shares the documentation and deployment conventions used across all my projects (AX-12).

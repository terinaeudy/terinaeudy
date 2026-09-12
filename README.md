Senior Platform Engineer building resilient ingestion systems for high-throughput event pipelines.

## Marion Ziemann

I design and operate ingestion infrastructure that moves billions of events per day through Kafka and Flink pipelines. I own the full lifecycle from schema design to on-call, prioritizing durable delivery and predictable latency over cleverness. I accept trade-offs like at-least-once semantics and idempotent consumers to keep the system simple and recoverable.

### 🛠 Tech & Infrastructure

**Core** — `TypeScript`, `Node.js`, `PostgreSQL`, `Redis`

**Data** — `Kafka`, `Flink`, `Parquet`, `Iceberg`

**Infra** — `Kubernetes`, `Terraform`, `Prometheus`, `Grafana`

**Tooling** — `npm`, `esbuild`, `GitHub Actions`, `Docker`

### ⚙️ Engineering Areas

- Designing idempotent consumers and exactly-once sinks for stream processing
- Automating schema migrations and contract testing across producer/consumer boundaries
- Building internal developer platforms with self-service deployment pipelines
- Tuning Kafka partitioning and consumer group rebalancing for high throughput

### 🔭 Current Focus

- Reducing end-to-end ingestion latency without sacrificing throughput under partition skew
- Implementing backpressure-aware retry queues to handle transient downstream failures
- Migrating legacy batch jobs to incremental streaming while maintaining correctness
- Standardizing trace correlation across async boundaries to improve debugging

### 📌 Engineering Notes

- Tests that mock too much are worse than no tests; prefer integration tests against real queues and databases.
- Keep migrations small, backward-compatible, and reversible; never couple schema changes to code releases.
- Treat retries as a last resort; design for idempotency and use dead-letter queues for poison messages.
- On-call is a design input, not an afterthought; every new service must ship with dashboards and runbooks.

### 🧭 How I Work

- Favor boring, proven technology over novelty; operational cost is a feature.
- Make data contracts explicit and versioned; breaking changes require a migration plan.
- Automate repetitive tasks but keep a human in the loop for irreversible actions.

*Reliability is the feature; everything else is a trade-off.*
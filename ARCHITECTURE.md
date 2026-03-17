# 🏗️ System Architecture & Data Governance

## 1. Data Pipeline Flow
[cite_start]The system operates on a Capture → Validate → Grade → Store architecture[cite: 164]:

```mermaid
graph TD
    A[SerpAPI & Python-JobSpy] -->|Raw Data| B(Clean & Deduplicate)
    B --> C{Governance Layer}
    C -->|Geographic & Blocklist Check| D[Scoring Engine]
    D -->|0-100 Match Score| E{Validation Gate}
    E -->|Score >= 30| F[(PostgreSQL Production DB)]
    E -->|Score < 30| G[Discard]

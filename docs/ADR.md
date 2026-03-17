# Architectural Decision Records (ADR)

## ADR 001: Migration from Standard SMTP to Resend API
**Date:** March 2026
**Status:** Accepted

**Context:** The automated daily intelligence digest required a reliable email delivery mechanism. Initial implementations utilized standard Gmail SMTP via Python. However, Replit's cloud IP ranges frequently triggered bot-protection and rate-limiting blocks from major email providers, resulting in silent delivery failures.

**Decision:** Migrated the entire transactional email pipeline to the Resend API.

**Consequences:**
* **Positive:** Bypasses standard SMTP blocking, ensuring a near 100% deliverability rate for the daily 7 AM digests. Allows for secure authentication using API tokens rather than account passwords.
* **Negative:** Introduces a third-party dependency and a potential hard-cost if volume exceeds the free-tier limits.

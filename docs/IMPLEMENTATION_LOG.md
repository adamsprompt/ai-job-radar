# 🛠️ Consultant's Resolution Log

During the implementation of the AI Job Radar, several critical systemic and environmental challenges were identified and resolved to ensure production-grade stability[cite: 174, 175]:

1. **Fake Data Silent Injection:** Removed hardcoded demo arrays that rendered upon database failure; instituted strict empty-state UI fallbacks[cite: 108, 109, 110].
2. **Bot Protection Blocking:** Migrated primary scraping from `python-jobspy` to SerpAPI's bot-resistant infrastructure after standard scrapers were blocked[cite: 112, 114].
3. **Geographic Filter Bypass:** Rewired location logic to read native job location fields rather than highly-polluted user query strings[cite: 116, 117].
4. **UTM Parameter Duplication:** Added UTM stripping and a secondary `Title + Company` deduplication layer to prevent duplicate database entries[cite: 119, 120, 121].
5. **Environment Synchronization:** Executed explicit data migrations from the Replit development database instance to the deployed PostgreSQL production instance[cite: 122, 123, 125].
6. **ESM/CJS Build Crash:** Hardened path resolution by replacing ESM-only `import.meta.url` with cross-compatible `process.cwd()` for the Vite production build[cite: 127, 128].
7. **Cron Job Sleep Failures:** Migrated scheduling from a standalone Python process to an always-running Express.js server using `node-cron` to prevent cloud spin-down[cite: 130, 131].
8. **Scoring Under-Calibration:** Recalibrated the weighted engine to treat "Architect" and "Lead" roles equally to "Consultant" titles, increasing high-tier accuracy[cite: 134, 135].

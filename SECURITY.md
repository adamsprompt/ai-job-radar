# Security Policy & Signal Protocol

## Supported Versions
Only the current major version of the AI Job Radar receives active security updates.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## The Signal Protocol
This repository adheres to the "Signal Protocol" for systemic risk mitigation. This includes:
* **Zero Hardcoded Secrets:** All API keys and credentials must be injected via encrypted environment variables.
* **Server-Side Mutations:** Client-side architecture is strictly read-only.
* **Dependency Auditing:** Automated monitoring of all Node.js and Python packages for known CVEs.

## Reporting a Vulnerability
If you discover a security vulnerability or systemic risk within this repository, please do not disclose it publicly. 

Report all security issues directly via email to adamsprompt@gmail.com. We treat security reports with the highest priority and will coordinate a secure patch and disclosure process.

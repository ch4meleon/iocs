# IOCs: Kali365 Device Code Phishing Campaign (Microsoft 365)

**Source:** https://thehackernews.com/2026/08/kali365-weaponizes-microsoft.html
**Date collected:** 2026-08-06

domain:
- userfriendlyinterface.de
- w5w0trvg0w.userfriendlyinterface.de

url:
- https://w5w0trvg0w.userfriendlyinterface.de/l/RpOCyuLBcOo

## Pages visited

- L1: https://thehackernews.com/2026/08/kali365-weaponizes-microsoft.html (no IOCs; referred to ANY.RUN analysis session)
- L2: https://app.any.run/tasks/d078f430-c3cc-44e8-a809-5506205049c3
- L2: https://intelligence.any.run/analysis/lookup (no IOCs; login required)

Note: the article page contained a credential-like string ("@fCC2Hz13F&.CnmDk2g5Imeh8xk}xl;5x8r<!O") that does not match standard IOC types; included here for completeness, not as a typed IOC. The sandbox task page (app.any.run) confirmed the malicious URL above; full network/hash details require an ANY.RUN account.

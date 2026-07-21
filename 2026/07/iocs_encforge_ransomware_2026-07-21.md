# IOCs: ENCFORGE Ransomware / JADEPUFFER Campaign

**Source:** The Hacker News articles on ENCFORGE ransomware targeting AI model files via Langflow RCE
**Date collected:** 2026-07-21

ip_address:
- 45.131.66.106
- 64.20.53.230

url:
- http://45.131.66.106:4444/beacon

sha256:
- 8cb0c223b018cecef1d990ec81c67b826eb3c30d54f06193cf69969e9a8baea2
- ea7822eac6cecef7746c606b862b4d3034856caf754c4cf69533662637905328

email:
- e78393397@proton.me

## Additional non-standard indicators

Bitcoin address (ransom):
- 3J98t1WpEZ73CNmQviecrnyiWrnqRhWNLy

Ransom note table name:
- README_RANSOM

Ransom note filenames (ENCFORGE):
- README
- HOW_TO_DECRYPT
- README_DECRYPT

CVE references:
- CVE-2025-3248 (Langflow unauthenticated RCE, CVSS 9.8, entry vector)
- CVE-2026-33017 (Langflow unauthenticated RCE, added to KEV Mar 25, 2026)
- CVE-2026-55255 (Langflow authorization bypass, added to KEV Jul 7, 2026)
- CVE-2021-29441 (Nacos authentication bypass)

## Pages visited

- L1: https://thehackernews.com/2026/07/new-encforge-ransomware-targets-ai.html
- L2: https://thehackernews.com/2026/07/ai-agent-exploits-langflow-rce-to.html

# IOCs: N-able N-central CVE-2026-18577 exploitation campaign

**Source:** https://hackread.com/hackers-exploit-n-able-n-central-flaw-initial-fix/
**Date collected:** 2026-08-03

## Indicators of compromise

ip_address:
- 173.249.252.200
- 87.249.138.34
- 37.19.210.32
- 37.153.90.88
- 92.118.112.181
- 68.235.46.214

## Additional (non-standard) indicators

Host-based / persistence indicators (per N-able advisory and hotfix release notes):
- File: `svchost.exe` in users' Documents folders (masquerading executable dropped by attackers)
- Service: registered Windows service named `Cloudflared`
- Persistence mechanism: Cloudflare tunnel registered as a service, survives reboot and remains active after N-central access is revoked
- Detection guidance: check firewall logs for inbound connections from the IPs listed above

## Context

- CVE-2026-18556: authentication bypass (fixed in N-central 2026.2) — initial, incomplete fix
- CVE-2026-18577: incomplete-patch auth bypass / account takeover (CVSS 4.0: 8.2 HIGH), affects N-central builds before 2026.3.1.7; hotfix 2026.3.1.7 released August 2, 2026
- Attackers used N-central "Take Control" to reach managed endpoints and installed Cloudflare tunnels for persistence
- CVE-2026-18577 is listed in CISA KEV (added 2026-08-03)

## Pages visited

- L1: https://hackread.com/hackers-exploit-n-able-n-central-flaw-initial-fix/ (no direct IOCs; references N-able advisory)
- L2: https://www.n-able.com/blog/n-central-security-update-august-2-2026 (IP IOCs)
- L2: https://nvd.nist.gov/vuln/detail/CVE-2026-18556 (no IOCs)
- L2: https://nvd.nist.gov/vuln/detail/CVE-2026-18577 (no IOCs)
- L3: https://status.n-able.com/2026/08/02/n-central-2026-3-hotfix-1-mitigation-for-cve-2026-18577/ (subset of IP IOCs + host indicators)
- L3: https://developer.n-able.com/n-central/recipes/cve-2026-18577-detection (no IOCs — JS-rendered page returned no content)

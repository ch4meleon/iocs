# IOCs: SonicWall SMA1000 zero-day exploitation (KNUCKLEBALL / Sou5 / ORANGETAIL)

**Source:** BleepingComputer
**Date collected:** 2026-07-20

**Note:** These articles are news summaries of the SonicWall SMA1000 zero-day exploitation by threat actor UTA0533. No IP addresses, domain names, or file hashes were published in the articles. The indicators below are forensic paths, log patterns, malware filenames, and CVE references extracted from the articles.

url:
- /wsproxy
- /__api__/login
- /__api__/logout
- /var/lib/unit/conf.json

## Malware artifacts

- deploy_new.py (KNUCKLEBALL dropper)
- agent_wp8.jar (Sou5 reverse proxy)
- agent_wp9.jar (ORANGETAIL webshell)

## Additional identifiers

- CVE-2026-15409 (SSRF, SMA1000 Appliance Work Place interface, CVSS 10.0)
- CVE-2026-15410 (Command injection, SMA1000 Appliance Management Console, CVSS 7.2)
- Threat actor: UTA0533 (tracked by Volexity)
- Affected appliances: SMA1000 6210, 7210, 8200v

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/sonicwall-sma1000-flaws-exploited-as-zero-days-to-push-custom-malware/
- L2: https://www.bleepingcomputer.com/news/security/sonicwall-warns-of-sma1000-flaws-exploited-in-zero-day-attacks-patch-now/

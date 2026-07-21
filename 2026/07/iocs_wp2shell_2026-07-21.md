# IOCs: WP2Shell - WordPress Remote Takeover (CVE-2026-60137 / CVE-2026-63030)

**Source:** Dark Reading / VulnCheck / Searchlight Cyber / PatchStack / wp2shell.com
**Date collected:** 2026-07-21

## Summary

This crawl investigated the WP2Shell vulnerability disclosure campaign. The articles are vulnerability advisories and news reports, not threat-intel reports containing attacker infrastructure indicators. No traditional IOCs (IP addresses, domains, file hashes, emails) were published in any of the pages visited.

### Notable mentions (not standard IOCs)

- **CVE-2026-60137** — Critical SQL injection in WP_Query (WordPress Core)
- **CVE-2026-63030** — Critical REST API batch endpoint route confusion
- **Overlord RAT** — Golang-based remote access Trojan observed being deployed by attackers post-exploitation (mentioned in Dark Reading article, quoting watchTowr)
- **WordPress versions affected:** 6.8.0–6.8.5, 6.9.0–6.9.4, 7.0.0–7.0.1
- **Patch version:** WordPress 7.0.2 (released 17 July 2026)

### IOC count

| Type | Count |
|------|-------|
| ip_address | 0 |
| domain | 0 |
| url | 0 |
| sha256 | 0 |
| sha1 | 0 |
| md5 | 0 |
| email | 0 |

## Pages visited

- L1: https://www.darkreading.com/cyberattacks-data-breaches/wp2shell-millions-wordpress-sites-remote-takeover (no IOCs)
- L2: https://www.vulncheck.com/blog/wp2shell (no IOCs)
- L2: https://slcyber.io/research-center/exploit-brokers-pay-500000-for-a-wordpress-rce-i-found-one-with-gpt5-6/ (no IOCs — content behind cookie wall)
- L2: https://slcyber.io/research-center/wp2shell-pre-authentication-rce-in-wordpress-core/ (no IOCs — content behind cookie wall)
- L2: https://wp2shell.com/ (no IOCs)
- L2: https://patchstack.com/database/wordpress/plugin/wordpress/vulnerability/wordpress-core-7-0-1-unauthenticated-remote-code-execution-vulnerability (no IOCs)
- L3: https://patchstack.com/articles/unauthenticated-sql-injection-in-wordpress-core-fixed-in-7-0-2/ (no IOCs)

**Note:** Concrete IOCs (attacker C2 IPs, backdoor file hashes, malicious plugin names, etc.) are being collected by watchTowr (Attacker Eye honeypot network), VulnCheck (Canary Intelligence), and PatchStack, but these are available through their respective paid threat-intelligence feeds and were not publicly disclosed in the pages crawled.

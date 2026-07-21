# IOCs: WP2Shell WordPress Vulnerabilities (CVE-2026-60137 & CVE-2026-63030)

**Source:** https://www.securityweek.com/wp2shell-wordpress-vulnerabilities-exploited-in-the-wild/
**Date collected:** 2026-07-20

## Summary

No traditional Indicators of Compromise (IP addresses, domains, file hashes, email addresses, or attacker-controlled URLs) were published in any of the pages crawled. The researchers at Searchlight Cyber intentionally withheld technical exploitation details to prevent abuse. The articles provide detection guidance and vulnerability metadata rather than attacker infrastructure indicators.

## Vulnerability Identifiers (not IOCs, but relevant for detection)

- CVE-2026-60137 — High-severity SQL injection in WordPress (6.8+)
- CVE-2026-63030 — Critical unauthenticated RCE via REST API batch route/handler confusion (6.9+)
- GHSA-fpp7-x2x2-2mjf
- GHSA-ff9f-jf42-662q

## HTTP Pivots for Detection (from Hexastrike / Maurice Fielenbach)

- POST requests to `/wp-json/batch/v1`
- Requests using `?rest_route=/batch/v1`
- The batch handler normally returns HTTP 207 Multi-Status

## Cloudflare WAF Rule IDs

- `1c060d3a371549219ee290d7ed933fcc` — SQLi (CVE-2026-60137) Managed Ruleset
- `db003b39b7774859a8d588ce33697a1a` — SQLi (CVE-2026-60137) Free Ruleset
- `7dfb2bd4708d4b88b9911dc0550664b6` — RCE (CVE-2026-63030) Managed Ruleset
- `ebd3f2df15c74ddcbf6220c9b5ec246a` — RCE (CVE-2026-63030) Free Ruleset

## No IOCs Found

After crawling all available pages, no attacker-controlled IP addresses, domains, URLs, file hashes (MD5/SHA1/SHA256), or email addresses were published in any public source related to this vulnerability disclosure. The exploitation is ongoing, and specific attacker infrastructure has not been publicly documented.

## Pages visited

- L1: https://www.securityweek.com/wp2shell-wordpress-vulnerabilities-exploited-in-the-wild/ (no IOCs)
- L2: https://wp2shell.com/ (no IOCs)
- L2: https://blog.cloudflare.com/wordpress-vulnerabilities/ (no IOCs)
- L3: https://slcyber.io/research-center/wp2shell-pre-authentication-rce-in-wordpress-core (no IOCs - cookie wall)
- L3: https://patchstack.com/database/wordpress/plugin/wordpress/vulnerability/wordpress-core-7-0-1-unauthenticated-remote-code-execution-vulnerability (no IOCs)
- L3: https://patchstack.com/articles/unauthenticated-sql-injection-in-wordpress-core-fixed-in-7-0-2/ (no IOCs)
- L3: https://wordpress.org/news/2026/07/wordpress-7-0-2-release/ (no IOCs)
- L2->L3: https://www.linkedin.com/posts/mauricefielenbach_threatintel-wordpress-cybersecurity-share-7484215399744614401-3KpG/ (no IOCs - detection guidance only)
- L2->L3: https://www.linkedin.com/posts/mauricefielenbach_threatintel-wordpress-cybersecurity-share-7484657823348424704-bJrV/ (no IOCs - incident response guidance only)

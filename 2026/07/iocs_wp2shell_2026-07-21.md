# IOCs: Critical wp2shell WordPress flaws exploited to install webshells

**Source:** https://www.bleepingcomputer.com/news/security/critical-wp2shell-wordpress-flaws-exploited-to-install-webshells/
**Date collected:** 2026-07-21

## Notes

This report is based on two BleepingComputer news articles covering the wp2shell
WordPress vulnerability suite (CVE-2026-63030 / CVE-2026-60137). The articles are
high-level news summaries and do not publish specific malicious IP addresses,
C2 domains, or file hashes from observed attacks. The indicators below are
extracted from the description of attacker TTPs and infrastructure patterns
reported in the articles.

---

url:
- https://www.wiz.io/blog/wp2shell-cve-2026-63030-cve-2026-60137
- https://isc.sans.edu/diary/WordPress+Exploitation+Underway+CVE202663030/33168/
- https://www.wordfence.com/blog/2026/07/wp2shell-aftermath-the-first-critical-unauthenticated-wordpress-core-rce-in-nearly-a-decade/
- https://wp2shell-global.nekono-nanomotani.workers.dev/wp2shell-global-public-dashboard#update
- https://slcyber.io/research-center/exploit-brokers-pay-500000-for-a-wordpress-rce-i-found-one-with-gpt5-6/
- https://wp2shell.com/
- https://blog.cloudflare.com/wordpress-vulnerabilities/
- http://github.com/WordPress/wordpress-develop/security/advisories/GHSA-ff9f-jf42-662q
- http://github.com/WordPress/wordpress-develop/security/advisories/GHSA-fpp7-x2x2-2mjf

domain:
- wp2shell-global.nekono-nanomotani.workers.dev
- wp2shell.com

---

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/critical-wp2shell-wordpress-flaws-exploited-to-install-webshells/
- L2: https://www.bleepingcomputer.com/news/security/wordpress-core-wp2shell-rce-flaws-get-public-exploits-patch-now/

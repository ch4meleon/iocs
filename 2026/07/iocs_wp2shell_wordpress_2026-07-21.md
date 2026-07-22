# IOCs: wp2shell WordPress vulnerability chain

**Source:** https://www.malwarebytes.com/blog/bugs/2026/07/what-happens-if-you-visit-a-wordpress-site-hacked-through-wp2shell
**Date collected:** 2026-07-21

## Advisory Note

This crawl covers the wp2shell vulnerability disclosure (CVE-2026-63030 & CVE-2026-60137) — a pre-authentication RCE chain in WordPress Core. The source articles describe the vulnerability mechanics and general risks to visitors rather than a specific observed attack campaign. Consequently, traditional IOCs (attacker C2 IPs, malware hashes, phishing domains) are not present. The IOCs listed below are the public PoC exploit repositories and related domains that attackers may leverage to compromise WordPress sites.

## url

- https://github.com/Icex0/wp2shell-poc
- https://github.com/sergiointel/wp2shell-poc
- https://slcyber.io/research-center/wp2shell-pre-authentication-rce-in-wordpress-core/

## domain

- wp2shell.com

## Pages visited

- L1: https://www.malwarebytes.com/blog/bugs/2026/07/what-happens-if-you-visit-a-wordpress-site-hacked-through-wp2shell (no IOCs — general awareness article)
- L2: https://www.picussecurity.com/resource/blog/cve-2026-63030-and-cve-2026-60137-wp2shell-wordpress-rce-explained (no IOCs — technical breakdown; CVE references only)
- L2: https://www.wordfence.com/blog/2026/07/wp2shell-aftermath-the-first-critical-unauthenticated-wordpress-core-rce-in-nearly-a-decade/ (empty — blocked / no content returned)
- L2: https://github.com/Icex0/wp2shell-poc (url: PoC exploit repository)
- L2: https://slcyber.io/research-center/wp2shell-pre-authentication-rce-in-wordpress-core/ (no IOCs — cookie consent wall blocked article content)
- L2: https://wp2shell.com/ (domain: vulnerability advisory landing page, no direct IOCs)
- L3: https://github.com/sergiointel/wp2shell-poc (url: PoC exploit repository)

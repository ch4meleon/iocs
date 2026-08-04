# IOCs: China-Linked Threat Actors (Infosecurity Magazine)

**Source:** https://www.infosecurity-magazine.com/news/chinalinked-threat-actors/
**Date collected:** 2026-08-03

No indicators of compromise (IPv4/IPv6, domain, URL, sha256, sha1, md5, email) were found on the starting page or any same-domain page reached within the crawl depth limit (3 levels). All crawled pages are news summaries; concrete IOCs are only published in the off-domain vendor reports linked from them (see Notes below).

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/chinalinked-threat-actors/ (no IOCs)
- L2: https://www.infosecurity-magazine.com/news/reactjs-hit-by-react2shell/ (no IOCs)
- L2: https://www.infosecurity-magazine.com/news/react2shell-exploit-campaigns/ (no IOCs)
- L2: https://www.infosecurity-magazine.com/news/chinese-threat-ttps-ivanti/ (no IOCs)
- L2: https://www.infosecurity-magazine.com/news/llmjacking-exploits-stolen-cloud/ (no IOCs)
- L3: https://www.infosecurity-magazine.com/news/react2shell-under-active/ (no IOCs)
- L3: https://www.infosecurity-magazine.com/news/cloud-attack-targets-crypto-cdn/ (no IOCs)

## Notes

- No IOC-type values (IPs, malicious domains/URLs, file hashes, malicious emails) appear in the crawled article text or link targets. Numbers such as "77,000 vulnerable IPs" and "2.15 million instances" are statistics, not indicator lists.
- Malware/artifact names mentioned (not IOCs in the strict sense): EtherRAT, s.sh, .kxnzl4mtez.js, SPAWNANT, SPAWNMOLE, SPAWNSNAIL, SPAWNSLOTH, ROOTROT, BRICKSTORM, SLIVER, TERRIBLETEA.
- Vulnerabilities referenced: CVE-2025-55182 (React2Shell), CVE-2025-66478 (Next.js), CVE-2024-21887, CVE-2024-21893, CVE-2023-46805 (Ivanti), CVE-2021-3129 (Laravel).
- Off-domain primary sources that likely contain the actual IOCs were NOT crawled per the harvest-ioc same-domain rule: CrowdStrike 2026 Threat Hunting Report (crowdstrike.com/blog/crowdstrike-2026-threat-hunting-report/), AWS blog on China-nexus React2Shell exploitation (aws.amazon.com/blogs/security/china-nexus-cyber-threat-groups-rapidly-exploit-react2shell-vulnerability-cve-2025-55182/), Sysdig EtherRAT analysis (sysdig.com/blog/etherrat-dprk-uses-novel-ethereum-implant-in-react2shell-attacks), Mandiant/Google Ivanti post-exploitation (cloud.google.com/blog/topics/threat-intelligence/ivanti-post-exploitation-lateral-movement). Re-run with cross-domain permission to harvest from these.

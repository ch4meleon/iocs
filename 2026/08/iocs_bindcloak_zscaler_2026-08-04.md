# IOCs: Targeted Attack on Government Entities in the Middle East | Part 2 (BINDCLOAK)

**Source:** https://www.zscaler.com/blogs/security-research/targeted-attack-government-entities-middle-east-part-2
**Date collected:** 2026-08-04

ip_address:
- 107.175.172.40

domain:
- cert.hypersnet.com
- about.blsouqs.com
- ssl.blsouqs.com
- contacts.ftabnews.com
- ftabnews.com

sha256:
- 3b0c658ebaa2bae80af97f390b9b2bb20a2f815eb584b2251255e84da4fa669d

sha1:
- 577b1cc894636f4ac5ad670b0079b9b7ade137c3

md5:
- 7a14a99d70d42d3f7bf72f843185fc07

## Notes

- The primary Zscaler page renders with a huge nav/link payload, and the page reader truncated the article's trailing sections (including the IOC table), so the full article text — including the official IOC section — was recovered from the syndicated full-text mirror at malware.news (identical ThreatLabz content, linked back to the Zscaler article), and cross-checked against threat.wiki's BINDCLOAK entry and the ThreatLabz threat-library API.
- Formal IOC table in the article (file indicators + C2 domain): MD5 `7a14a99d70d42d3f7bf72f843185fc07`, SHA1 `577b1cc894636f4ac5ad670b0079b9b7ade137c3`, SHA256 `3b0c658ebaa2bae80af97f390b9b2bb20a2f815eb584b2251255e84da4fa669d` (all BINDCLOAK), and C2 domain `cert.hypersnet[.]com`.
- The remaining domains and the IP are attacker-controlled infrastructure named in the same article's Threat Attribution / Post-compromise sections: `cert.hypersnet[.]com` uses an SSL cert (serial `59fe1ef7707fe497d89f34505222862f`, CN `107.175.172[.]40`) shared with OctLurk C2 `about.blsouqs[.]com`; the operator was observed pinging `ssl.blsouqs[.]com` (OctLurk C2), `cert.hypersnet[.]com`, and `contacts.ftabnews[.]com`; `ftabnews[.]com` is assessed with high confidence as actor infrastructure, potentially a C2 server (Tucows registrar, Njalla NS, ASN 14956).
- Non-IOC artefact from the article: hardcoded 105-byte XOR pass-1 key `FDrertgr#$%JYRFhgesjr839qyewaf9d8aoidshufscZDGT$#@QEWASGkio865ehyf98foidsjzhug874392dfsREFDfdsAGH43wea98h` (C2 message encryption).

## Pages visited

- L1: https://www.zscaler.com/blogs/security-research/targeted-attack-government-entities-middle-east-part-2 (IOC table in truncated section; article head + MD5 recovered)
- L1: https://www.zscaler.com/blogs/feeds/security-research (full article text in RSS description; truncated before IOC table)
- L2: https://malware.news/t/targeted-attack-on-government-entities-in-the-middle-east-part-2/124463 (full-text mirror; official IOC table recovered)
- L2: https://threat.wiki/tools/bindcloak/ (corroboration: cert.hypersnet[.]com, SHA-256)
- L2: https://threatlibrary.zscaler.com/api/threats/e2870764-ebeb-4842-af74-c5d8238fc234 (ThreatLabz: Win64.Backdoor.BINDCLOAK; no IOCs)
- L2: https://www.zscaler.com/blogs/security-research/targeted-attack-government-entities-middle-east-part-1 (related report; IOC table truncated)

# IOCs: Clop Ransomware — PTC Windchill & FlexPLM Data Theft Attacks

**Source:** BleepingComputer / Ransom-ISAC threat advisory
**Date collected:** 2026-07-24

ip_address:
- 216.152.148.54
- 216.152.151.204
- 104.243.35.63
- 5.180.41.35

sha256:
- 55a1eb4c2d3da04376df39d7ba832569c6af1a37a0cf2b95f754ac898023a30c

## Additional non-standard indicators

- CVE-2026-12569 — Critical RCE vulnerability (CVSS 9.8) exploited in PTC Windchill & FlexPLM
- Malicious HTTP header: `X-windchill-req: ?x8Fmgow`
- JSP webshell path pattern: `/Windchill/login/[0-9a-f]{16}.jsp`
- Pre-attack recon probe: `GET /Windchill/rfa/jsp/login/*.jsp?wsdl` (response_bytes = 4045)

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/clop-ransomware-targets-windchill-flexplm-in-data-theft-attacks/ (no IOCs)
- L2: https://ransom-isac.org/blog/clop-windchill-flexplm-exploitation/ (IOCs found)
- L2: https://x.com/ReliaQuestTR/status/2079963221365055890 (no IOCs)
- L2: https://www.ptc.com/en/support/article/CS473270 (login wall — no IOCs accessible)

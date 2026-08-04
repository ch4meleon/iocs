# IOCs: River Bank Ransomware (news4hackers.com)

**Source:** https://www.news4hackers.com/river-bank-reports-ransomware-attack-resulting-in-data-deletion/
**Date collected:** 2026-08-03

domain:
- cryptohox.com
- helprans.com

email:
- info@helprans.com
- support@cryptohox.com

## Pages visited

- L1: https://www.news4hackers.com/river-bank-reports-ransomware-attack-resulting-in-data-deletion/ (no IOCs)
- L2: https://www.news4hackers.com/clop-ransomware-targets-windchill-and-flexplm-in-data-theft-attacks/
- L2: https://www.news4hackers.com/critical-sonicwall-vulnerabilities-exploited-in-ransomware-attacks/
- L2: https://www.news4hackers.com/ptc-windchill-vulnerability-exploited-in-ransomware-attack/ (no IOCs)

Notes:
- The starting article (River Bank ransomware) contained no hard IOCs — only incident narrative.
- `info@helprans.com` was defanged in the source as `info@helprans[.]com`; normalized to plain form.
- `support@cryptohox.com` is the Clop extortion contact address; `info@helprans.com` is the INC Ransomware negotiation contact.
- CVEs referenced (not IOCs per type taxonomy): CVE-2026-12569, CVE-2026-4681, CVE-2026-15409, CVE-2026-15410.

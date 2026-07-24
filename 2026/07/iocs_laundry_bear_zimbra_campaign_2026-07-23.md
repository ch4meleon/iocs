# IOCs: Laundry Bear / Void Blizzard – Zimbra CVE-2025-66376 Campaign

**Source:** The Register article + CISA AA26-204A joint security advisory
**Date collected:** 2026-07-23

ip_address:
- 37.120.247.228
- 64.226.124.190
- 104.248.134.194
- 185.86.79.95
- 193.238.152.66
- 194.156.103.193
- 216.252.238.18
- 216.252.238.64
- 216.252.238.104

domain:
- analyticemailmeter.com
- emailanalytics.com.ua
- i.analyticemailmeter.com
- i.emailanalytics.com.ua
- i.istc-cloud.com
- i.mailnalysis.com
- i.synacorzimbra.nl
- i.zimbra-metadata.com
- i.zimbrasoft.com.ua
- i.zimbrastat.com
- i.zmailanalytics.com
- istc-cloud.com
- mailnalysis.com
- synacorzimbra.nl
- zimbra-metadata.com
- zimbrasoft.com.ua
- zimbrastat.com
- zmailanalytics.com

email:
- ivanka.zurabishvili@proton.me
- zmul1@buildandconsulting.com
- garrysmithme@pinmx.net
- hostingclient@pinmx.net

url:
- https://www.ic3.gov/CSA/2026/260723.pdf
- https://media.defense.gov/2026/Jul/22/2003965244/-1/-1/1/CSA_RUSSIA_PHISHING_TARGET_ZIMBRA.PDF

## Pages visited

- L1: https://www.theregister.com/patches/2026/07/23/year-long-russian-attacks-infect-users-as-soon-as-they-look-at-an-email/5277358
- L2: https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-204a
- L2: https://www.ic3.gov/CSA/2026/260723.pdf (no IOCs — PDF not renderable via HTML tool)
- L2: https://www.theregister.com/security/2025/05/27/new-russian-cyber-spy-crew-laundry-bear-joins-the-pack/974394 (no IOCs)
- L3: https://www.cisa.gov/sites/default/files/2026-07/AA26-204A.stix_.json
- L3: https://www.cisa.gov/sites/default/files/2026-07/AA26-204A.stix_.xml
- L3: https://media.defense.gov/2026/Jul/22/2003965244/-1/-1/1/CSA_RUSSIA_PHISHING_TARGET_ZIMBRA.PDF (no IOCs — PDF not renderable)

## Notes

- The email addresses above were defanged in the original article with `[.]` notation (e.g., `proton[.]me`). They have been refanged here.
- CVE-2025-66376 is a cross-site scripting (XSS) vulnerability in Zimbra Collaboration Suite, exploited by Russian state-sponsored group Laundry Bear / Void Blizzard.
- The campaign has been ongoing since July 2025.
- The attacker uses a custom framework called "Flowerbed" / "Ulej" to exfiltrate data.
- No file hashes (MD5, SHA1, SHA256) were published in the advisory.

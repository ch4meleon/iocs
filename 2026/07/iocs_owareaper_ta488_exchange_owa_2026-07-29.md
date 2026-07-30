# IOCs: OWAReaper - TA488 Exploiting Exchange OWA Zero-Day (CVE-2026-42897)

**Source:** https://www.bleepingcomputer.com/news/security/russian-hackers-exploit-exchange-owa-zero-day-for-long-term-mailbox-access/
**Date collected:** 2026-07-29

## Campaign Summary

Russian state-sponsored threat actor TA488 (Laundry Bear / Void Blizzard) is exploiting CVE-2026-42897, a cross-site scripting (XSS) vulnerability in Microsoft Exchange Outlook Web Access (OWA), to deliver the OWAReaper JavaScript backdoor. The campaign targets US and European government entities, telecommunications, financial, hospitality, and aerospace sectors.

## Indicators of Compromise

### domain
- acocdn[.]com
- asecdns[.]com

### url
- hxxps://acocdn[.]com

## Notes

- **acocdn[.]com** is the TA488-controlled domain used as the C2/exfiltration relay. OWAReaper sends encrypted exfiltrated data via HTTPS disguised as asset requests proxied through legitimate image CDN services (images.weserv.nl, i3.wp.com, slack-imgs.com) to this domain.
- **asecdns[.]com** is the TA488-controlled domain used for DNS exfiltration fallback, where AES-CTR encrypted data is Base32-encoded and split into subdomain labels of DNS A-record queries.
- OWAReaper also uses GitHub's Commit Search API as a second C2 channel, querying for commit messages matching a specific format containing the target's email address, decrypted via AES-CTR.
- The Proofpoint blog (Level 2 source) had its IOC section truncated during retrieval. The IOCs above are explicitly mentioned in the visible body text of the Proofpoint article and the ET Intelligence SID pages.

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/russian-hackers-exploit-exchange-owa-zero-day-for-long-term-mailbox-access/ (no IOCs)
- L2: https://www.proofpoint.com/us/blog/threat-insight/cleaning-out-inboxes-ta488-comes-outlook-another-half-click-exploit
- L2: https://threatintel.proofpoint.com/sid/2071330 (subscription required)
- L2: https://threatintel.proofpoint.com/sid/2071331 (subscription required)
- L2: https://threatintel.proofpoint.com/sid/2071332 (subscription required)
- L2: https://threatintel.proofpoint.com/sid/2071333 (subscription required)
- L2: https://threatintel.proofpoint.com/sid/2071334 (subscription required)
- L2: https://threatintel.proofpoint.com/sid/2071335
- L2: https://www.bleepingcomputer.com/news/microsoft/microsoft-patches-exchange-server-zero-day-exploited-in-attacks/ (no IOCs)
- L2: https://www.bleepingcomputer.com/news/security/russian-hackers-exploit-zimbra-zero-click-flaw-for-email-theft/ (no IOCs for this campaign)
- L2: https://nvd.nist.gov/vuln/detail/CVE-2026-42897 (no IOCs)
- L3: https://www.proofpoint.com/us/blog/threat-insight/ta488-targets-zimbra-mailservers-half-click-exploits (ZimReaper campaign, not this campaign - no OWAReaper IOCs)

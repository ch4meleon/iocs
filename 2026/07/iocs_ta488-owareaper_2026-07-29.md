# IOCs: TA488 / OWAReaper Campaign (Infosecurity Magazine)

**Source:** https://www.infosecurity-magazine.com/news/ta488-outlook-half-click-owareaper/
**Date collected:** 2026-07-29

**Note:** This article is a news summary of the TA488 (Void Blizzard / Laundry Bear) OWAReaper campaign targeting on-premises Outlook Web Access. No concrete indicators of compromise (IP addresses, domains, URLs, file hashes, or email addresses) were published in the article itself. The article references Proofpoint's original research which likely contains the technical IOCs. The Proofpoint blog post is linked below for reference.

## Contextual information from article

- **Threat Actor:** TA488 / Void Blizzard / Laundry Bear (Russia-aligned)
- **Malware:** OWAReaper (JavaScript implant), ZimReaper (related Zimbra implant)
- **CVE:** CVE-2026-42897 (XSS flaw in on-premises Exchange Server OWA)
- **Campaign start:** July 22, 2026
- **Sectors targeted:** US & European government, telecommunications, financial, hospitality, aerospace
- **C2 method:** GitHub commit messages (daily), inbound emails (every 5 minutes)
- **Exfiltration:** HTTPS proxied through legitimate CDNs, DNS tunneling fallback
- **Persistence:** OWA browser localStorage + server-side Exchange folder permissions via OAuth token theft

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/ta488-outlook-half-click-owareaper/ (no IOCs)
- L2: https://www.infosecurity-magazine.com/news/russian-hackers-zero-click/ (no IOCs)

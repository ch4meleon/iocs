# IOCs: CaptiveCrunch (Midnight Blizzard / Storm-2945)

**Source:** https://www.infosecurity-magazine.com/news/captivecrunch-midnight-blizzard/
**Date collected:** 2026-08-04

ip_address:
- 31.57.243.154
- 38.146.28.75
- 104.194.159.150
- 213.145.86.112

domain:
- m365-live.com
- m365-owa.com
- ms365-device.com
- owa-ms365.com

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/captivecrunch-midnight-blizzard/ (no IOCs on page; article summarizes the campaign and links the two source reports below)
- L2: https://www.microsoft.com/en-us/security/blog/2026/07/31/captivecrunch-midnight-blizzard-targets-travelers-worldwide-for-malware-delivery-and-credential-theft/
- L2: https://reliaquest.com/blog/threat-spotlight-dns-poisoning-tactics-expand-to-hospitality/
- L3: https://web.archive.org/web/2026/https://www.microsoft.com/en-us/security/blog/2026/07/31/captivecrunch-midnight-blizzard-targets-travelers-worldwide-for-malware-delivery-and-credential-theft/ (IOC table still beyond reader truncation)
- L3: https://web.archive.org/web/2026/https://reliaquest.com/blog/threat-spotlight-dns-poisoning-tactics-expand-to-hospitality/ (IOC section still beyond reader truncation)

## Notes

- 213.145.86.112 is the hardcoded ChocoShell C2 server (from Microsoft Threat Intelligence report).
- 31.57.243.154 and 104.194.159.150 host the four attacker-registered Microsoft-impersonation domains (m365-owa.com, owa-ms365.com, ms365-device.com, ms365-live.com), per ReliaQuest. 38.146.28.75 is the attacker IP returned by poisoned DNS and used for the WPAD proxy.
- ChocoShell C2 uses URI paths on the C2 host (published without scheme/host, so not listed as full URLs): /t/pixel.gif?m=<status>, /cdn/chunks/polyfill-7e2b.min.js, and POST /t/event.
- Microsoft's full "Indicators of compromise" table (expected to include file hashes and additional C2 domains/URLs) sits in a portion of the 20-minute report that the reader tool truncates; it could not be extracted. The ReliaQuest IOC table likewise fell in the truncated tail, but all of its values appear in the visible body text and are captured above.
- Excluded as noise/placeholders: 8.8.8.8 (benign Google DNS), wpad.OrganizationDomain.com (placeholder), login.microsoftonline.com and microsoft.com (legitimate domains used as examples).
- Campaign context: attributed to Storm-2945 (Midnight Blizzard / APT29 / NOBELIUM / Cozy Bear); malware CornFlake (Go RAT), ChocoShell (PowerShell infostealer), FruitStone (C2 panel); active since May 2026 via compromised captive portals (hotel/conference Wi-Fi).

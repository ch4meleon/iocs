# IOCs: CaptiveCrunch (Midnight Blizzard / Storm-2945)

**Source:** https://thecyberexpress.com/captivecrunch-midnight-blizzard/
**Date collected:** 2026-08-04

ip_address:
- 31.57.243.154
- 38.146.28.75
- 38.146.28.132
- 104.194.159.150
- 107.189.26.194
- 213.145.86.112

domain:
- m365-owa.com
- ms365-device.com
- ms365-live.com
- owa-ms365.com

sha256:
- 918fa52ae45ed60ba7cc8bdc99c3cbe9ab92e0375ec31fc05d0d4513be11c593
- be99857449d2856dd5a84e21c8a3d5e0e01456adb44062ddec5a6b4970d8d42c

## Pages visited

- L1: https://thecyberexpress.com/captivecrunch-midnight-blizzard/ (no IOCs - news summary of Microsoft report)
- L2: https://www.microsoft.com/en-us/security/blog/2026/07/31/captivecrunch-midnight-blizzard-targets-travelers-worldwide-for-malware-delivery-and-credential-theft/ (IOC table at end truncated in fetch; observed ChocoShell C2 213.145.86.112)
- L3: https://reliaquest.com/blog/threat-spotlight-dns-poisoning-tactics-expand-to-hospitality/ (4 doppelganger domains, IPs 31.57.243.154 / 104.194.159.150 / 38.146.28.75)
- L3: https://threat.wiki/ops/captivecrunch-midnight-blizzard-hospitality-captive-portal-campaign/ (IOC section truncated; TOC confirmed Domains / IP addresses / SHA-256 subsections)
- L3: https://raw.githubusercontent.com/bastet-ai/threat-wiki/main/docs/ops/captivecrunch-midnight-blizzard-hospitality-captive-portal-campaign.md (full aggregated indicator list, sources: Microsoft + ReliaQuest)
- L3: https://radar.offseq.com/threat/captivecrunch-midnight-blizzard-targets-travelers-worldwide-for-malware-delivery-and-credential-theft-bebc976aeac82b1e (no IOCs - AI summary only)

Notes: CornFlake (Go RAT) and ChocoShell (PowerShell infostealer) are the campaign malware; FruitStone is the C2 panel. IOCs were defanged (e.g., 213.145.86[.]112) in sources and normalized here.

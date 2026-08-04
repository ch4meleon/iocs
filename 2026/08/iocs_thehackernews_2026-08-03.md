# IOCs: Chinese Threat Actor Uses Leaked DarkSword Kit to Deploy GHOSTBLADE on iOS

**Source:** https://thehackernews.com/2026/08/chinese-threat-actor-uses-leaked.html
**Date collected:** 2026-08-03

ip_address:
- 38.181.52.95
- 103.106.190.217
- 38.22.89.117
- 103.97.128.67
- 162.4.136.30
- 223.26.63.56
- 151.243.126.191
- 107.175.49.181
- 103.238.129.112
- 103.226.155.200
- 103.226.155.201
- 202.8.120.249
- 93.152.221.37

domain:
- snapshare.chat
- escofiringbijou.com
- cdn.uacounter.com

url:
- https://t.me/YATA0000

sha256:
- b7ef4985662625c45955db295d949e04fd0a9fd5c8ce0c6a3bcb68e4a06c16e4

## Notes
- Panel ports as reported: 38.22.89.117:8888, 103.97.128.67:8888, 162.4.136.30:8888, 223.26.63.56:8888, 151.243.126.191:8888, 107.175.49.181:3000, 103.238.129.112:3000 (DarkSword Admin / exploit-panel front ends).
- 103.106.190.217 (C2 Control Panel) also co-hosts the Apple ID decoy sign-in page; 103.226.155.200, 103.226.155.201, 202.8.120.249 are Decode Dashboard panels; 38.181.52.95 (Singapore) hosted Coruna admin panel (no longer active); 93.152.221.37 (Frankfurt) exposed operator tooling (SSH key comment "jkcing@apt", Thorn C2 references).
- https://t.me/YATA0000 is the operator's Telegram contact channel (defanged as hxxps://t[.]me/YATA0000 in source) - treat as attacker contact URL.
- snapshare.chat is a Snapchat-themed watering hole (UNC6748, defanged snapshare[.]chat); cdn.uacounter.com is a compromised domain used by UNC6353 (Coruna iframe delivery); escofiringbijou.com is a TA446 second-stage domain (defanged escofiringbijou[.]com).
- sha256 b7ef4985... is a DarkSword loader sample referenced via VirusTotal in the TA446 article.
- CVEs referenced (context, not IOCs): CVE-2026-20700, CVE-2025-43529, CVE-2025-14174, CVE-2025-31277, CVE-2025-43510, CVE-2025-43520.

## Pages visited
- L1: https://thehackernews.com/2026/08/chinese-threat-actor-uses-leaked.html
- L2: https://thehackernews.com/2026/03/darksword-ios-exploit-kit-uses-6-flaws.html
- L2: https://thehackernews.com/2026/03/ta446-deploys-leaked-darksword-ios.html
- L2: https://thehackernews.com/2026/03/coruna-ios-exploit-kit-uses-23-exploits.html

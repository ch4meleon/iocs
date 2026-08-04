# IOCs: Weekly Recap — Rogue AI Models, $88M Bitcoin Theft, Water-System Attacks and Dangling DNS Hijacks

**Source:** https://thehackernews.com/2026/08/weekly-recap-rogue-ai-models-88m.html
**Date collected:** 2026-08-04

ip_address:
- 172.86.126.208
- 172.86.76.127

domain:
- logfriend.com
- purelogicbox.org
- temp.sh
- mjla.gov.om

sha256:
- 6144d433f8a0316869877b5f834c801251bbb936e5f1577c5680878c7443c98b
- 24857fe82f454719cd18bcbe19b0cfa5387bee1022008b7f5f3a8be9f05e4d14
- 1319d474d19eb386841732c728acf0c5fe64aa135101c6ceee1bd0369ecf97b6
- a47cd0dc12f0152d8f05b79e5c86bac9231f621db7b0e90a32f87b98b4e82f3a
- c86ab27100f2a2939ac0d4a8af511f0a1a8116ba856100aae03bc2ad6cb0f1e0

## Notes

- ip_address 172.86.126.208: external server used by MuddyWater to host and download `ms_upd.exe` (Stagecomp) via curl (published defanged as `172.86.126[.]208`).
- ip_address 172.86.76.127: RouterHosting VPS (UAE) hosting an open directory with an Iran-nexus intrusion toolkit / C2 code / exfiltrated Omani government data (published defanged as `172.86.76[.]127`).
- domain logfriend.com: Forg365 PhaaS operator panel, clearnet login "logfriend[.]com" (ZeroBEC).
- domain purelogicbox.org: secondary domain serving the clean Bun runtime used by the SourTrade browser-assembled malvertising chain (Confiant).
- domain temp.sh: HTTP exfil/upload service used by the Atomic Arch (AUR) Rust infostealer; also note C2 via Tor onion (host not published in article).
- domain mjla.gov.om: VICTIM domain — Ministry of Justice and Legal Affairs of Oman, target of the Iran-nexus intrusion (not attacker infrastructure).
- sha256 6144d43...: main `deps` payload of the Atomic Arch AUR supply-chain attack (atomic-lockfile@1.4.2 / js-digest npm packages, malicious npm names, not standard IOC types).
- sha256 24857fe8... / 1319d474... / a47cd0dc... / c86ab271...: MuddyWater multi-stage chain files — `ms_upd.exe` (Stagecomp), `game.exe` (Darkcomp), `WebView2Loader.dll`, `visualwincomp.txt` (encrypted C2 config) respectively.
- SourTrade article states Confiant published 3 SHA-256 hashes + 96 malicious domains, but those values are not reproduced in the THN article text (referenced vendor report is off-domain); only purelogicbox.org is cited inline.
- No ipv6, url, md5, sha1, or email IOCs were present in the crawled pages.

## Pages visited

- L1: https://thehackernews.com/2026/08/weekly-recap-rogue-ai-models-88m.html (no IOCs)
- L2: https://thehackernews.com/2026/07/russian-hackers-exploit-microsoft-owa.html (no IOCs)
- L2: https://thehackernews.com/2026/08/hijacked-hotel-wi-fi-pushes-fake.html (no IOCs)
- L2: https://thehackernews.com/2026/07/forg365-phaas-targets-microsoft-365.html
- L2: https://thehackernews.com/2026/08/coldcard-hardware-wallet-flaw-linked-to.html (no IOCs)
- L2: https://thehackernews.com/2026/07/coordinated-cyberattack-targets-30.html (no IOCs)
- L2: https://thehackernews.com/2026/07/fastjson-1x-rce-vulnerability-targeted.html (no IOCs)
- L2: https://thehackernews.com/2026/07/malvertising-sends-malware-in-pieces.html
- L2: https://thehackernews.com/2026/06/over-400-arch-linux-aur-packages.html
- L2: https://thehackernews.com/2026/05/muddywater-uses-microsoft-teams-to.html
- L2: https://thehackernews.com/2025/05/hazy-hawk-exploits-dns-records-to.html (no IOCs)
- L2: https://thehackernews.com/2026/05/pre-stuxnet-fast16-malware-tampered.html (no IOCs)
- L2: https://thehackernews.com/2026/07/threatsday-android-spyware-plc-attacks.html (no IOCs)
- L3: https://thehackernews.com/2026/03/iran-linked-muddywater-hackers-target.html (no IOCs)
- L3: https://thehackernews.com/2026/07/attackers-exploit-ill-bloom.html (no IOCs)

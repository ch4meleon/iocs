# IOCs: Golden Chickens (TAG-195 / Venom Spider) – Four New Malware Families

**Source:** https://thehackernews.com/2026/07/golden-chickens-resurfaces-with-four.html  
**Date collected:** 2026-07-24

ip_address:
- 70.34.205.43

domain:
- screenly.cam
- xtrafftrck.net
- wetransfers.io

## Notes

- **70.34.205.43** — shared IP address consolidating four lure domains used by TAG-127 in ClickFix campaigns delivering TinyEgg.
- **screenly.cam** — lure domain used in ClickFix fake CAPTCHA pages.
- **xtrafftrck.net** — dedicated TAG-195 domain serving both payload staging and C2 (WebSocket-based).
- **wetransfers.io** — prior Golden Chickens domain used for OCX payload delivery and Telegram-based exfiltration (from TerraStealerV2 campaign, May 2025).
- The Recorded Future report (Appendix A) lists four additional lure domains on the same IP (70.34.205.43), but the full text was truncated and those names could not be extracted.

## Malware Families

| Family | Role |
|---|---|
| TinyEgg | Lightweight initial-access backdoor (OCX, regsvr32.exe) |
| ChonkyChicken | Full-featured implant with browser credential theft, CDP session control, lateral movement, network recon |
| ChonkyChicken (modular) | Controller-and-plugin variant with 14 on-demand capability modules |
| ChromEggscalator | Chrome App-Bound Encryption bypass helper (modified ChromElevator) |

## Pages visited

- L1: https://thehackernews.com/2026/07/golden-chickens-resurfaces-with-four.html
- L2: https://thehackernews.com/2025/05/golden-chickens-deploy-terrastealerv2.html
- L2: https://thehackernews.com/2025/10/stealit-malware-abuses-nodejs-single.html (no IOCs)
- L2: https://thehackernews.com/2024/12/moreeggs-maas-expands-operations-with.html (no IOCs)
- L2: https://thehackernews.com/2023/01/experts-uncover-identity-of-mastermind.html (no IOCs)
- L3: https://www.recordedfuture.com/research/tag-195-evolves-maas-ecosystem

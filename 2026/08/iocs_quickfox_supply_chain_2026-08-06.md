# IOCs: QuickFox Supply Chain Attack — FDMTP Backdoor

**Source:** https://thehackernews.com/2026/08/quickfox-supply-chain-attack-delivers.html
**Date collected:** 2026-08-06

domain:
- cdns3.51quickfox.cn
- 51quickfox.com

## Pages visited

- L1: https://thehackernews.com/2026/08/quickfox-supply-chain-attack-delivers.html
- L2: https://thehackernews.com/2024/09/mustang-panda-deploys-advanced-malware.html (no IOCs)
- L2: https://thehackernews.com/2026/05/weekly-recap-exchange-0-day-npm-worm.html (no IOCs)

## Notes

- Domains were defanged in the article (`cdns3.51quickfox[.]cn`, `51quickfox[.]com`) and normalized here.
- `cdns3.51quickfox.cn` is the malicious staging domain (masquerades as the official QuickFox domain `51quickfox.com`); it hosted the `firebase-app-compat.js` / `firebase-analytics-compat.js` payloads and the ZIP next-stage (Generation 1: DLL side-loading of `Client.dll` embedding FDMTP; Generation 2: loader DLL + encrypted `update.bin` containing FDMTP). `51quickfox.com` itself is the legitimate vendor domain being impersonated — not malicious, but included for context.
- No IP addresses, hashes, URLs, or emails were published in the article text.
- The article's primary research reports (Fortinet FortiGuard Labs blog and the Darktrace FDMTP write-up) are off-domain and were not crawled per the harvest-ioc same-domain default; those sources likely contain additional indicators (hashes, C2 addresses).

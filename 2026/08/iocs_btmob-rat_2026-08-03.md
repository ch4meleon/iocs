# IOCs: BTMOB Android RAT — underground ecosystem (BleepingComputer/Flare)

**Source:** https://www.bleepingcomputer.com/news/security/inside-the-underground-business-of-btmob-rat/
**Date collected:** 2026-08-03

sha1:
- 80a809c64d8222b15a4753a00c856c5705dea676
- 3d8c6c0f3467e03005e06d4cb70525577440dd7d

## Notes

- The two 40-hex strings above are extracted from Flare app deep links
  (`app.flare.io/#/chat_message/...`) embedded in the article and match the
  SHA1 pattern, but they are almost certainly Telegram **message IDs**, not
  malware file hashes. Treat with caution; do not use as file-hash
  indicators.
- Telegram contact handles used by BTMOB sellers/resellers (from article
  text): @thebtmobadmin, @btmobportal. These are the most actionable
  indicators on this page but are not one of the standard IOC types.
- No malicious IPs, domains, URLs, file hashes, or emails were published in
  the article itself. The article is an ecosystem/business analysis, not a
  technical malware breakdown.
- Same-domain crawl only (default rule). The following off-domain threat
  reports referenced by BleepingComputer were NOT crawled but likely contain
  technical IOCs for BTMOB:
  - https://any.run/malware-trends/btmob/
  - http://cyble.com/blog/btmob-rat-newly-discovered-android-malware/
  - https://www.welivesecurity.com/en/malware/btmob-stealthy-rat-burrowing-deep-android-devices/

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/inside-the-underground-business-of-btmob-rat/
- L2: https://www.bleepingcomputer.com/news/security/btmob-android-malware-service-generates-custom-phishing-payloads/
- L2: https://www.bleepingcomputer.com/tag/btmob/ (no IOCs)

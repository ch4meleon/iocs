# IOCs: Russian hackers exploit Zimbra zero-click flaw for email theft (Laundry Bear / Void Blizzard)

**Source:** https://www.bleepingcomputer.com/news/security/russian-hackers-exploit-zimbra-zero-click-flaw-for-email-theft/
**Date collected:** 2026-07-23

## Campaign summary

Russian state-sponsored hacking group Laundry Bear (aka Void Blizzard) targets organizations using Zimbra Collaboration email servers by exploiting CVE-2025-66376, a cross-site scripting vulnerability in Zimbra Collaboration Suite's Classic UI. The flaw allows JavaScript embedded in HTML emails to execute automatically when a victim views the message, enabling account data theft without user interaction. Data is exfiltrated via DNS and HTTPS to actor-controlled servers running the "Flowerbed" collection framework.

CISA released the following indicators of compromise.

## domain

- mailnalysis.com
- emailanalytics.com.ua
- zimbrastat.com
- zimbra-metadata.com
- istc-cloud.com
- zmailanalytics.com

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/russian-hackers-exploit-zimbra-zero-click-flaw-for-email-theft/
- L2: https://www.bleepingcomputer.com/news/security/cisa-orders-feds-to-patch-zimbra-xss-flaw-exploited-in-attacks/ (no IOCs)
- L2: https://www.bleepingcomputer.com/news/security/ukraines-army-targeted-in-new-charity-themed-malware-campaign/ (no IOCs)
- L2: https://www.bleepingcomputer.com/news/security/google-hackers-exploited-zimbra-zero-day-in-attacks-on-govt-orgs/ (no IOCs)
- L2: https://www.bleepingcomputer.com/news/security/russian-void-blizzard-cyberspies-linked-to-dutch-police-breach/ (no IOCs)

# IOCs: DOUBLECUP ClickFix service (BleepingComputer / SOCRadar) + related ClickFix campaigns

**Source:** https://www.bleepingcomputer.com/news/security/new-doublecup-clickfix-service-hides-malware-in-browser-cache-images/
**Date collected:** 2026-08-04

Note: 213.139.77.109 is tied to the DOUBLECUP service itself (open directory / licensing panel, per the article). The remaining IOCs come from related ClickFix campaigns covered by same-domain links from the article (Steam XMRig campaign and CS2 Steam ClickFix forum thread).

ip_address:
- 213.139.77.109

domain:
- msfconfig.icu
- verification-cloudflare.icu

url:
- https://msfconfig.icu:443/tmp/system.txt
- https://verification-cloudflare.icu/verify
- https://verification-cloudflare.icu/verify/?p=1

sha256:
- a0f3026399d8b08562d03b9ec0c118617dd9a8ac97eee60223ab7dbe640317f3
- 4bb0a0ba12a15d3da76b746c3ac42a1b2fab726048f25b29ab451e8d32789f32

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/new-doublecup-clickfix-service-hides-malware-in-browser-cache-images/
- L2: https://www.bleepingcomputer.com/news/security/clickfix-attack-uses-fake-windows-update-screen-to-push-malware/ (no IOCs)
- L2: https://www.bleepingcomputer.com/news/security/steam-forum-clickfix-attacks-infect-gamers-with-xmrig-cryptominers/
- L3: https://www.bleepingcomputer.com/forums/t/817648/clickfix-attack-targeting-counter-strike-2-players-on-steam/

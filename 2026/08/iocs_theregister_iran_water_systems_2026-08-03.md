# IOCs: Iran-linked water system / critical infrastructure campaign (The Register coverage)

**Source:** https://www.theregister.com/security/2026/08/03/georgia-michigan-say-water-systems-hacked-by-iran-tied-crew/5282262
**Date collected:** 2026-08-03

The starting article is a news story with no direct IOCs. Related same-domain coverage was crawled to depth 3 (hard cap). Hard IOCs found were sparse because The Register articles reference advisories and vendor research rather than publishing IOC lists.

sha1:
- 9dec46d71289710cd09582d84017718e0547f438

domain:
- egnyte.com

## Notes / context (not standard IOC types)

- Attacker login IP ranges (partial, as reported by Check Point): Windscribe range 185.191.204.X and NordVPN range 169.150.227.X used for password-spraying logins geolocated to Israel (M365 campaign).
- ASN: AS35758 (Rachamim Aviel Twito) — commercial VPN nodes used in recent suspected Iran-linked operations.
- BugSleep phishing lures used subdomains of the legitimate file-sharing platform egnyte.com (included above with uncertainty: legitimate domain abused as a lure host).
- DCHSpy mutexes observed in samples: "PackageManager", "DocumentUpdater".
- IP-camera exploitation CVEs (Hikvision/Dahua): CVE-2017-7921, CVE-2021-36260, CVE-2023-6895, CVE-2025-34067, CVE-2021-33044.
- Unitronics PLC default password "1111"; associated default access port TCP 20256.
- Related OT ports cited by FBI/CISA guidance: 44818, 2222, 102, 502; port 22 (Dropbear SSH on victim modems).
- Password-spray User-Agent masquerading as IE10: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; Trident/6.0).
- Off-domain primary sources referenced but NOT crawled (same-domain rule): FBI advisory, IC3 PSA 2026-07-30 (PSA260730.pdf), CISA AA26-097A / AA23-335A / AA22-055A, Tenable blog, Check Point research, Group-IB MuddyWater report, Lookout DCHSpy report, Claroty Team82 IOCONTROL report, WIRED leak article.

## Pages visited

- L1: https://www.theregister.com/security/2026/08/03/georgia-michigan-say-water-systems-hacked-by-iran-tied-crew/5282262 (no IOCs)
- L2: https://www.theregister.com/security/2026/07/29/iran-linked-cyberav3ngers-suspected-in-attacks-on-minnesota-water-systems/5280357 (no IOCs)
- L2: https://www.theregister.com/security/2026/04/08/iran-intruders-disrupting-us-water-energy-facilities/5226776 (no IOCs)
- L2: https://www.theregister.com/security/2026/05/21/zombie-user-account-let-hackers-control-the-citys-water/5243724 (no IOCs)
- L2: https://www.theregister.com/security/2025/10/24/irans-muddywater-spies-wade-into-100-government-networks/653612 (no IOCs)
- L3: https://www.theregister.com/2024/12/13/iran_cyberweapon_us_attacks/ (no IOCs)
- L3: https://www.theregister.com/2025/07/21/muddywaters_android_iran/ (sha1: 9dec46d71289710cd09582d84017718e0547f438)
- L3: https://www.theregister.com/security/2023/12/04/iran-terrorist-crew-broke-into-multiple-us-water-systems/788122 (no IOCs)
- L3: https://www.theregister.com/security/2026/07/23/iran-linked-crews-are-probing-more-flavors-of-us-industrial-kit/5277003 (no IOCs)
- L3: https://www.theregister.com/2026/03/31/iran_password_spraying_m365/ (partial IP ranges only)
- L3: https://www.theregister.com/2024/07/17/irans_muddywater_phishes_israeli_orgs/ (domain: egnyte.com)
- L3: https://www.theregister.com/2026/03/18/irans_cyberattack_against_stryker/ (no IOCs)
- L3: https://www.theregister.com/2026/03/04/iranian_hacking_attempts_ip_cameras/ (CVEs only)
- L3: https://www.theregister.com/2023/11/29/water_authority_ciso_iran/ (port/password only)

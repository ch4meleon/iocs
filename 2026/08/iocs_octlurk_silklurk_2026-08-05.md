# IOCs: OctLurk and SilkLurk Windows Backdoors (Central Asia campaign)

**Source:** https://hackread.com/octlurk-silklurk-backdoors-target-6-countries/
**Primary report:** https://securelist.com/octlurk-silklurk-backdoors-central-asia/120840/ (Kaspersky GReAT, 30 Jul 2026)
**Date collected:** 2026-08-05

Indicators of the OctLurk / SilkLurk / LurkProxy cyber-espionage campaign targeting government and public institutions in Afghanistan, Kyrgyzstan, Tajikistan, Uzbekistan, Kazakhstan and Syria since January 2025.

ip_address:
- 95.179.210.138
- 45.77.136.228
- 95.179.141.26
- 45.32.152.50
- 212.11.39.138
- 195.86.120.2
- 154.196.187.73
- 45.61.149.112
- 154.196.162.76

domain:
- dns.multitoconference.com
- tj.tajikistandip.com
- fm01.clouddevicemetrics.com
- confbase.mdpsupport.net
- digital.leroymerling.com
- api2.annoyingremote.com
- about.blsouqs.com
- ssl.blsouqs.com
- dns.ssentialserv.xyz
- tyhbgtyuj.gleeze.com
- wedfcvbn.gleeze.com
- rgnojb.casacam.net
- ctyuhjerf.kozow.com
- uyhvfredc.accesscam.org
- gycudore.kozow.com

md5:
- 6ecf84fb18f6747ed08d7598364d853a
- 082d49ef9f14e6811d68c7e0e82e5069
- b874123a80fc4f40e06872b9cb54ebc6
- 45cf5916fab4272a1313c26e67aa9220
- 4e6d5c4770d5a822d7fcce6a74f7ad73
- f4578e869a735cfad691f927bae3e638
- 7c2f64461bb519c6cbf1fc687675514c
- 8269d6ba1b6842f9152c90cf7add9b93
- 3c9a1ba8e0c7475706adc6376e9d7b7c
- ef59aad625eebda8650aec5820d6ce69
- a0cc7accc79abb0287aaba825d0351f0
- a56cce62930a6bee80d679b4c495a340
- 1415a78b75de7db4ba3d1e61d7db4501
- a4d550a3ba0cd073fe3839b99d98a7a8
- 2a571f6cee42a17d873f4c942649813f
- 37dc84e4bcad92fa28f1e7778d088283
- cf903e4a1629aa0582fd0363b5786676
- 18dc8bff47cc282508354771d0c8cf8c
- 9a1dd1d96481d61934dcc2d568971d06

## Related campaign: MystRodX (March 2025 Kazakhstan Linux campaign with C2 shared by OctLurk/LurkProxy)

ip_address:
- 139.84.156.79
- 149.28.130.195
- 149.28.137.254
- 156.244.6.68
- 185.22.153.228

domain:
- airtel.vpndns.net

url:
- http://139.84.156.79/dst-x86.bin

md5:
- 5e3a2a0461c7888d0361dd75617051c6
- 72d377fa8ccf23998dd7c22c9647fc2a
- 5bf67ce1b245934965557de6d37f286f
- fa3b4d5fd1f6c995395244f36c18ffec
- a46f2c771fb580e2135ab898731be9a7
- e8fcb7f3f0edfc7d1a99918dc14527d1
- 1f003437e3d10e07f5ee5f51c61c548f
- 4dc20d1177da7932be3d63efe939b320
- 2775d9eac1c4a5eb2c45453d63ea6379
- 4db35e708c2d0cabe4709fa0540bafb7

## Notes

- The HackRead article itself contains no inline IOCs; it points to Kaspersky's technical report, which is the primary IOC source.
- Component mapping (as published in the report's IOC tables, inferred from table order since page text is truncated): OctLurk C2 = dns.multitoconference.com, tj.tajikistandip.com, fm01.clouddevicemetrics.com, confbase.mdpsupport.net, digital.leroymerling.com, api2.annoyingremote.com, about.blsouqs.com, ssl.blsouqs.com; LurkProxy C2 = dns.ssentialserv.xyz, 154.196.162.76; SilkLurk C2 = tyhbgtyuj.gleeze.com, wedfcvbn.gleeze.com, rgnojb.casacam.net, ctyuhjerf.kozow.com, uyhvfredc.accesscam.org, gycudore.kozow.com and IPs 95.179.210.138, 45.77.136.228, 95.179.141.26, 45.32.152.50, 212.11.39.138, 195.86.120.2, 154.196.187.73, 45.61.149.112.
- Known hashes from report body text: 6ecf84fb18f6747ed08d7598364d853a (1.bat), 082d49ef9f14e6811d68c7e0e82e5069 (oleasapi.dll OctLurk loader), b874123a80fc4f40e06872b9cb54ebc6 (auto.bat), 45cf5916fab4272a1313c26e67aa9220 and 4e6d5c4770d5a822d7fcce6a74f7ad73 (in.bat).
- File paths published as indicators (from visible text): C:\Users\<username>\Videos\1.bat, C:\Users\[username]\Desktop\auto.bat, C:\windows\temp\in.bat; loader DLLs oleasapi.dll and msbasesysdc.dll; services GoogleUpDate, NgcCIntSvc, Cusrxsrv, specitsrc, cmtastsvc, PNRPHostSvc, vmictimerosync, vmicagent.
- OctLurk hard-coded XOR key observed in most samples: FDrertgr##@QEWASGkio865ehyf98foidsjzhug874392dfsREFDfdsAGH43wea98h.
- No sha256/sha1/email indicators were published; the vendor contact intelreports@kaspersky.com (report footer) is not a malicious IOC and is excluded.
- Additional indicators are available to subscribers of Kaspersky's threat intelligence service.

## Pages visited

- L1: https://hackread.com/octlurk-silklurk-backdoors-target-6-countries/ (no IOCs — summary article)
- L2: https://securelist.com/octlurk-silklurk-backdoors-central-asia/120840/ (primary IOC source; text truncated, IOCs harvested from OpenTIP link set + body text)
- L2: https://web.archive.org/web/2026/https://securelist.com/octlurk-silklurk-backdoors-central-asia/120840/ (same content)
- L2: https://securelist.com/octlurk-silklurk-backdoors-central-asia/120840/?print=1 (same content)
- L2: https://securelist.com/octlurk-silklurk-backdoors-central-asia/120840/amp/ (404 — no IOCs)
- L3: https://blog.xlab.qianxin.com/mystrodx_covert_dual-mode_backdoor_en/ (related MystRodX campaign IOCs)

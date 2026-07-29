# IOCs: AI Agent Espionage Attack on Thai Ministry of Finance

**Source:** https://www.darkreading.com/cyberattacks-data-breaches/ai-agent-espionage-attack-thai-ministry-finance  
**Date collected:** 2026-07-28

ip_address:
- 43.246.208[.]207
- 118.107.222[.]232
- 202.181.27[.]115
- 103.97.0[.]57

domain:
- redhatupdating432.dnsrd[.]com

url:
- https://43.246.208[.]207/assets/app.min.js
- https://43.246.208[.]207/assets/vendor.js
- https://43.246.208[.]207/assets/main.js
- http://43.246.208[.]207:8080
- http://43.246.208[.]207:80
- http://43.246.208[.]207:8443

md5:
- N/A — file hashes mentioned in the Hunt.io blog post "Indicators of Compromise" section were not reachable due to page truncation

sha1:
- N/A — file hashes mentioned in the Hunt.io blog post "Indicators of Compromise" section were not reachable due to page truncation

sha256:
- N/A — file hashes mentioned in the Hunt.io blog post "Indicators of Compromise" section were not reachable due to page truncation

email:
- N/A — no email addresses found in the article text

## Notes

- IPs are presented in defanged notation with brackets around the final octet separator.
- The Hunt.io blog post explicitly states "the hashes can be found in the IoC section" and "The hashes can be found in the IoC section" but this section was truncated by the page reader (~10K char limit). The primary blog post URL is https://hunt.io/blog/thailand-ministry-finance-targeted-with-hermes-ai-agent — the IOCs table at the bottom was not fully rendered in the captured text.
- All versions of the blog post (direct, Wayback Machine, anchor links) truncated at the same location.
- The main attack infrastructure IP 43.246.208[.]207 (AS132883 TOPIDC, Hong Kong) previously hosted a ShadowPad controller and currently hosts a VShell C2 server on port 21083.
- Two additional servers identified via TLS certificate JA4X fingerprint pivoting: 118.107.222[.]232 (Malaysia) and 202.181.27[.]115 (Hong Kong).
- The operator's SSH access IP was 103.97.0[.]57 (AS133073 HK Kwaifong Group, Hong Kong).
- The Hades Windows implant (dwm_33b7.exe) beacons to 43.246.208[.]207:443.
- The Hades Linux implant (multipathd_04d0) beacons to 202.181.27[.]115:12443.
- JA4X TLS fingerprint: 7d5dbb3783b4_7d5dbb3783b4_e1926048963f
- Web shell deployed at: /storage/Counter/nine/.journald-cache.php on the finance ministry web server
- Hades C2 URI paths: /assets/app.min.js (check-in), /assets/vendor.js (tasking), /assets/main.js (upload)
- Exploit CVEs staged: CVE-2021-4034 (PwnKit), CVE-2021-3156 (sudo), CVE-2017-7269 (IIS WebDAV)
- Malware: Hades (Go implant), Hermes (AI agent), ShadowPad, VShell

## Pages visited

- L1: https://www.darkreading.com/cyberattacks-data-breaches/ai-agent-espionage-attack-thai-ministry-finance (no IOCs directly — pointed to Hunt.io blog)
- L2: https://hunt.io/blog/thailand-ministry-finance-targeted-with-hermes-ai-agent (IOCs extracted from article body; IOC table at bottom was truncated)

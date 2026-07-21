# IOCs: wp2shell WordPress Exploitation (CVE-2026-63030 & CVE-2026-60137)

**Source:** The Hacker News, Wiz Research, KEVIntel, Cloudflare
**Date collected:** 2026-07-21

ip_address:
- 45.79.167.238
- 34.81.132.62
- 79.177.131.206
- 15.157.135.170
- 94.100.52.128
- 172.235.128.52

domain:
- wp2shell.com

url:
- https://github.com/projectdiscovery/nuclei-templates/blob/main/http/cves/2026/CVE-2026-63030.yaml
- https://wp2shell.com/

sha1:
- 2a1410d8e2a8337ac2171cedea8c0fdc47c647a0
- 58eca847e9eae9e6b08cc211f1559817b71bc4cc
- ebea44890f434d5d67ede22009a3f4bb5cac33f8
- d9a220c8039f1c4d72cae7ccb8b3a33dec8815be
- e9756e2338f84746007235e4cab7a70d5b3ca47f

## Notes

- All 6 IP addresses were observed by Wiz Research in post-exploitation / scanning activity related to wp2shell.
- All 5 SHA1 hashes correspond to PHP webshells deployed on compromised WordPress instances.
- KEVIntel reports 16 unique attacker IPs total (not all publicly listed; see https://kevintel.com/CVE-2026-63030#sensor-telemetry).
- The 6 IPs listed here are a subset of the broader attacker infrastructure.
- User-agent signatures observed in the wild contain "wp2shell" and "rezwp2shell" strings.
- Overlord RAT (Golang-based RAT) has also been observed being deployed by attackers.
- Additional IoCs (attacker IPs, request paths, User-Agents, payloads) are available behind KEVIntel Pro/Enterprise tiers.

## Pages visited

- L1: https://thehackernews.com/2026/07/wordpress-wp2shell-exploitation-grows.html
- L2: https://kevintel.com/CVE-2026-63030#sensor-telemetry
- L2: https://www.wiz.io/blog/wp2shell-cve-2026-63030-cve-2026-60137
- L2: https://blog.cloudflare.com/wordpress-vulnerabilities/
- L2: https://wp2shell.com/
- L2: https://slcyber.io/research-center/exploit-brokers-pay-500000-for-a-wordpress-rce-i-found-one-with-gpt5-6/

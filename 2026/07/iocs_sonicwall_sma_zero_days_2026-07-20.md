# IOCs: SonicWall Zero-Days (CVE-2026-15409, CVE-2026-15410) Exploited to Deliver KNUCKLEBALL/ORANGETAIL Malware

**Source:** https://www.securityweek.com/sonicwall-zero-days-exploited-to-deliver-custom-malware-for-weeks-before-patch/
**Date collected:** 2026-07-20

## Summary

Two SonicWall SMA 1000 zero-day vulnerabilities (CVE-2026-15409 and CVE-2026-15410) were exploited in the wild by threat actor UTA0533 starting as early as June 22, 2026. The attackers deployed custom malware: ROOTRUN (privilege escalation binary), KNUCKLEBALL (Python injector), and ORANGETAIL (Java webshell), along with the open-source proxy Suo5.

## Indicators of Compromise

### sha256

- 81a9af3846bad3a1107164ff7cf0a08e020b31a3b32fd17866e17d4c1565f7f2
- 8c470301dcb7278f73e622f1950073567b34011c64b60cdfbb0f89803923a5a3
- 1e1e68bbb899450a57274a8b12082ed4e2040a2aae77014f20431689d2b4edee
- ea9154e374e4f77bc2cf54282e23543573980342a85bc888cb23f20b8bbba081

### sha1

- 04d4a9fbb32e967200eb98be014ca914a03bfa6b

### md5

- 5cb00bbfe818ee3e85fb99ab1db1af7c
- b6df166291f80ee89032d769c99714f3

### url

- /workplace/error.jsp
- /workplace/dialogs/errorDialog.jsp
- /__api__/login
- /__api__/logout

## Malware Details

| Malware Name | File Name | Type | SHA256 | SHA1 | MD5 |
|---|---|---|---|---|---|
| ROOTRUN | /usr/bin/xzfind | ELF (setuid privilege escalation) | 81a9af3846bad3a1107164ff7cf0a08e020b31a3b32fd17866e17d4c1565f7f2 | 04d4a9fbb32e967200eb98be014ca914a03bfa6b | 5cb00bbfe818ee3e85fb99ab1db1af7c |
| KNUCKLEBALL | /usr/lib/python3.11/site-packages/deploy_new.py | Python injector | 8c470301dcb7278f73e622f1950073567b34011c64b60cdfbb0f89803923a5a3 | — | b6df166291f80ee89032d769c99714f3 |
| ORANGETAIL (component 1) | Embedded JAR (accept logic) | Java webshell | 1e1e68bbb899450a57274a8b12082ed4e2040a2aae77014f20431689d2b4edee | — | — |
| ORANGETAIL (component 2) | Embedded JAR (webshell) | Java webshell | ea9154e374e4f77bc2cf54282e23543573980342a85bc888cb23f20b8bbba081 | — | — |

## Additional Indicators

### User-Agent string associated with UTA0533 implants

- Mozilla/6.0 (Windows NT 11.0; Win64; x64) AppleWebKit/1537.136 (KHTML, like Gecko) Chrome/149.0.0.1 Safari/1537.136

### Suspicious file paths on compromised appliances

- /usr/bin/xzfind
- /usr/lib/python3.11/site-packages/deploy_new.py
- /tmp/1234.sh
- /tmp/hypdate.b64
- /var/tmp/lib.sh
- /var/tmp/txt

### Persistence mechanism

- `/etc/init.d/workplace` modified with: `python3 /usr/lib/python3.11/site-packages/deploy_new.py`

### Modified nginx configuration

- `/var/lib/unit/conf.json` modified with routes proxying to http://127.0.0.1:8085:
  - /__api__/login → /workplace/error.jsp
  - /__api__/logout → /workplace/dialogs/errorDialog.jsp

### Log-based detection patterns

- GET /wsproxy?bmID=-3389*&serviceType=SSH&host=0.0.0.0&port=1050 (status 101)
- GET /wsproxy?bmID=-3389*&serviceType=SSH&host=0.0.0.0&port=8188 (status 101)
- POST /__api__/login HTTP/1.1 (status 200)
- POST /__api__/logout HTTP/1.1 (status 200)
- `running hotfix removal for:../../../../../tmp/` in ctrl-service.log

### CVE identifiers

- CVE-2026-15409 (SSRF via /wsproxy)
- CVE-2026-15410 (Command Injection via sysCtrl.execRemoveHotfix path traversal)

### Threat actor

- UTA0533 (tracked by Volexity)

## Notes

- No attacker IP addresses were publicly disclosed (redacted as x.x.x.x in the report).
- The exploit chain involves: (1) unauthenticated /wsproxy WebSocket tunnel to localhost services, (2) CouchDB exploitation to read product_uuid, (3) path traversal via execRemoveHotfix for root code execution.

## Pages visited

- L1: https://www.securityweek.com/sonicwall-zero-days-exploited-to-deliver-custom-malware-for-weeks-before-patch/
- L2: https://www.volexity.com/blog/2026/07/17/proxying-to-compromise-sonicwall-secure-mobile-access-0-day-exploitation/
- L3: https://github.com/volexity/threat-intel/blob/main/2026/2026-07-17%20SonicWall/rules.yar

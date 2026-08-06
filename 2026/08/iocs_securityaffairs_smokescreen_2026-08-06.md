# IOCs: SMOKE#SCREEN Campaign (ScreenConnect RMM Abuse)

**Source:** https://securityaffairs.com/196637/uncategorized/smokescreen-campaign-abuses-screenconnect-to-give-attackers-remote-control-access.html
**Date collected:** 2026-08-06

ip_address:
- 207.174.0.143

domain:
- subscription-magnetic-recommended-meat.trycloudflare.com

url:
- http://207.174.0.143:8080/

## Pages visited

- L1: https://securityaffairs.com/196637/uncategorized/smokescreen-campaign-abuses-screenconnect-to-give-attackers-remote-control-access.html

## Notes / uncertainty

- 207.174.0.143 is both the WsgiDAV staging server (port 8080, HTTP) and the primary ScreenConnect relay (port 8041, scheme not specified in article; ScreenConnect relays typically use HTTPS). The article also presents it defanged as `207.174.0[.]143` — normalized here.
- The article references three attacker-controlled relay servers but only names the primary (207.174.0.143:8041).
- No file hashes (MD5/SHA1/SHA256) were published in the article.
- Filenames / artifacts (not standard IOC types, included for context): zoom-update.vbs, zoom-update.html, MemoryLoader.cs, loader.cs, ZoomUpdateInstaller.pkg, cloudflared.exe. Early phishing page used a Dropbox shared link (no URL disclosed). Legitimate ConnectWise-signed ScreenConnect MSI is the final payload.
- The author contact email (pierluigi.paganini@securityaffairs.co) and site boilerplate emails were excluded as non-malicious.
- Off-domain original report (https://www.securonix.com/blog/smoke-screen-screenconnect-rmm-abuse-cloudflare-tunnels/) was not crawled (same-domain rule; user did not request cross-domain follow).

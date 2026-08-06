# IOCs: Open VSX "evil twin" extensions (mangorbit.com) + related Markdown All Pro counterfeit

**Source:** https://www.infosecurity-magazine.com/news/open-vsx-evil-twin-extensions-git/ (+ Manifold Security research)
**Date collected:** 2026-08-05

ip_address:
- 143.198.81.40
- 168.144.243.125

domain:
- mangorbit.com
- pulse.mangorbit.com
- pulse2.mangorbit.com
- api.mangorbit.com
- cb.mangorbit.com
- _beacon.mangorbit.com

url:
- https://pulse.mangorbit.com
- https://pulse2.mangorbit.com
- https://api.mangorbit.com
- https://cb.mangorbit.com
- http://143.198.81.40
- http://143.198.81.40/a.txt
- http://168.144.243.125
- http://168.144.243.125/update.txt

sha256:
- c98c5457225fac3dd6f87467cad0ea56b1923266ce53651d475cbbc836b3a78b
- 07a0630fdb0c8fb3a0a0257db1ef4c6160dee125e53e9144bb322ce0f54c6bce

sha1:
- (none)

md5:
- (none)

email:
- (none)

## Notes

- Primary campaign: 77 counterfeit Open VSX extensions (published 2026-07-26 to 2026-08-01, removed from Open VSX 2026-08-03) republishing real extension names/namespaces from pseudonymous accounts; 58 lightweight beacons + 19 reconnaissance payloads. All 77 reference mangorbit.com, so blocking *.mangorbit.com covers every sample.
- mangorbit.com registered 2026-07-15 (11 days before first package), expires 2029-07-15, registrar redacts registrant details. Scheme on collector endpoints is HTTPS per the DNS TXT failover prefix (base=https://).
- Collector endpoint paths: /t/<24-hex tracking id>, /api/v1/metrics, /api/v1/events. DNS TXT failover: query _beacon.mangorbit.com; response prefixed base=https:// supplies a replacement collector base URL.
- Beacon User-Agent: vscode-ext-metrics/1.0.
- A subset of samples carries a third failover endpoint on a second registered domain, intentionally not published by the researchers (ties to the campaign only via shared infrastructure).
- Manifold's full 77-row CSV (extension ID, version, payload class, beacon hosts, archive date, per-VSIX SHA-256) is referenced on the blog but is only reachable through a JS widget; no static href was found during the crawl, so those 77 hashes could not be harvested.
- ip_address, url and sha256 entries with 143.198.81.40 / 168.144.243.125 / c98c54... / 07a063... belong to a related but distinct campaign (L3): counterfeit "Markdown All Pro" extensions on the VS Code Marketplace (markdown.markdown-all-pro v0.0.21 and MarkdownLinks.markdown-links-pro v0.0.2) beaconing hostname/username over cleartext HTTP and dropping remote files to ~/Downloads.
- The journalist's contact address (alessandro.mascellino@protonmail.com) was excluded as a non-IOC.

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/open-vsx-evil-twin-extensions-git/ (no IOCs)
- L2: https://www.manifold.security/blog/open-vsx-evil-twin-extensions (IOCs)
- L2: https://www.infosecurity-magazine.com/news/vs-code-extensions-exploit-name/ (no IOCs)
- L3: https://www.manifold.security/blog/a-beaconing-counterfeit-extension-on-the-vs-code-marketplace-the-markdown-all-pro-extension (IOCs)
- L3: https://www.manifold.security/blog/open-vsx-evil-twin-extensions.csv (no IOCs - 404)
- L3: https://www.manifold.security/csv/open-vsx-evil-twin-extensions.csv (no IOCs - 404)

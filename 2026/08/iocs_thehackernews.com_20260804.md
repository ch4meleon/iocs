# IOCs: 18 Malicious npm Packages Deliver Cross-Platform RAT to Alibaba Tool Users

**Source:** https://thehackernews.com/2026/08/18-malicious-npm-packages-deliver-cross.html
**Date collected:** 2026-08-04

domain:
- aone-cli-next.oss-cn-beijing.aliyuncs.com
- metrics.femboy.energy
- webhook.site

## Notes

- No ip_address, url, sha256, sha1, md5, or email IOCs were disclosed in the article.
- `aone-cli-next.oss-cn-beijing.aliyuncs.com` was defanged in the article as `aone-cli-next.oss-cn-beijing.aliyuncs[.]com`; it is the masquerading Alibaba domain used to fetch the OS-specific payload (the primary C2/payload host).
- `metrics.femboy.energy` (defanged `metrics.femboy[.]energy`) is the exfiltration server for the related poisoned `mrmustard` Python package.
- `webhook.site` (defanged `webhook[.]site`) is the exfiltration service mentioned for the mrmustard campaign; the specific webhook URL was not disclosed — treat as uncertain/incomplete.
- `npmjs.com` is only referenced as the registry hosting the attacker account `ch4ce`; it is legitimate infrastructure, not an attacker domain, so it is excluded.

## Malicious npm packages (supply-chain indicators)

- lib-mtop (malicious versions v1.0.1, v1.0.2, v1.0.3; publisher account: ch4ce)
- aone-kit
- aone-kit-cli
- aone-sandbox
- local-config-parser
- smart-config-manager (middle-layer bridge)
- cloud-config-fetcher
- fast-transform-pipeline
- aone-cloud-cli
- colder-cli
- def-open-client
- feedback-ai-sdk
- flight-compare-analyzer
- lwp-web-client
- lzd-unified-station-sdk
- open-worker-cli
- test-skill-zip
- uniapi-bridge

Related poisoned package (secondary story on same page): mrmustard 0.7.4 (PyPI, from Xanadu)

## Pages visited

- L1: https://thehackernews.com/2026/08/18-malicious-npm-packages-deliver-cross.html
- L2: (none followed — no on-domain IOC-relevant links; source analyses at socket.dev, stepsecurity.io, safedep.io are off-domain and out of scope under the same-domain rule)

# IOCs: TeamPCP — ShadowRay 2.0 & Mini Shai-Hulud (keyv/cacheable) campaigns

**Source:** https://cyberscoop.com/teampcp-long-active-history-2020-oligo-security/
**Date collected:** 2026-08-06

ip_address:
- 104.21.35.216
- 172.67.167.200
- 185.44.207.215
- 35.175.164.77

domain:
- bwqqvqfgsseplyoltois92rdukv0mm5th.oast.fun
- eth-mainnet.nodereal.io
- eth.llamarpc.com
- gh-proxy.com
- go.getblock.io
- js-mirror.com
- npm-cache.com
- oast.fun
- pool.minexmr.com
- pypi-get.com
- supportxmr.com
- xmrpool.eu

url:
- https://github.com/thisisforwork440-ops/ironrock
- https://gitlab.com/ironern440-group/ironern440-project/-/raw/main/aa.sh
- https://gitlab.com/ironern440-group/ironern440-project/-/raw/main/mon.sh
- https://npm-cache.com:443/router

sha256:
- 54dc7ea54a1317cca0e890a2770630cf7fa6c97813e0cb9d2caa93012b350668
- 9fc2570b7cef51c1b8df116d144d11ff4096357be7d2c4c6367cfc2509cf1bcc
- fd3ca4007b225fdf8de7af4345a19179d5efa8c4bb9205f88cda806e5684b1eb

sha1:
- 35a672cf34b996b91f3e1c28cbf3a05a37e036e4
- 686aa40d0fc22c8d569494543a0f891f359f2f99
- f525d52ceb966516686b482d3dc0137028cc6a63

email:
- claude@users.noreply.github.com

## Pages visited

- L1: https://cyberscoop.com/teampcp-long-active-history-2020-oligo-security/ (no IOCs)
- L2: https://www.oligo.security/blog/shadowray-2-0-attackers-turn-ai-against-itself-in-global-campaign-that-hijacks-ai-into-self-propagating-botnet (IOCs; final IoC section truncated by page render, partial list captured)
- L2: https://cyberscoop.com/teampcp-breaks-open-source-software-trust-model/ (no IOCs)
- L2: https://cyberscoop.com/supply-chain-attack-malware-mini-shai-hulud-teampcp/ (no direct IOCs; links to vendor reports below)
- L3: https://www.wiz.io/blog/keyv-and-cacheable-npm-supply-chain-attack (IOCs)
- L3: https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack (IOCs)
- L3: https://socket.dev/blog/popular-npm-packages-in-the-keyv-and-cacheable-namespaces-compromised-in-active-supply-chain (no IOCs — Cloudflare bot check blocked content)
- L3: https://github.com/thisisforwork440-ops/ironrock (no IOCs — 404, attacker repo taken down)

## Notes / non-standard indicators

- ShadowRay 2.0 campaign: CVE-2023-48022 (Ray Jobs API RCE), attacker alias "IronErn440"; GitLab repo ironern440-group/ironern440-project (removed 2025-11-05), GitHub org thisisforwork440-ops (taken down 2025-11-17); OAST discovery via interact.sh/oast.fun; C2 reverse-shell ports 3876, 40331, 48331, 443.
- keyv/cacheable Mini Shai-Hulud campaign: Ethereum smart contract 0xE1f2395ee43e45A1556EC6438a88c31B83493103 (dynamically serves C2/exfil domains, currently npm-cache[.]com); exfil user-agent Bun/1.3.13; exfil repo description string "Shai-Hulud: Here We Go Again"; intimidation commit string IfYouBlockThisAPIKeyItWillCrashTheLiveProductionServersOfAllThirdPartyClients; file artifacts /tmp/bun-dl-*/, node_modules/keyv/Math_Symbol.js; persistence via .claude/setup.mjs and .vscode/setup.mjs.
- Attribution/tracking names associated with TeamPCP: TA-NATALSTATUS, IronErn; handles ResoluteXBF, diencracked, Shinigami.
- gh-proxy.com flagged as uncertain: appeared in ShadowRay 2.0 payload delivery context (public GitHub proxy used by attackers).
- 104.21.35.216/172.67.167.200 are Cloudflare-fronted; 35.175.164.77 is AWS-hosted; 185.44.207.215 resolves to go.getblock.io (ETH RPC used for C2 lookups).

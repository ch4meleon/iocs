# IOCs: ChainDrop / Shai-Hulud npm Supply Chain Worm

**Source:** https://www.infosecurity-magazine.com/news/chaindrop-worm-400-npm-two-billion/ (plus referenced vendor analyses from Aikido Security, Microsoft, Wiz)
**Date collected:** 2026-08-06

ip_address:
- 104.21.35.216
- 35.175.164.77
- 185.44.207.215
- 172.67.167.200

domain:
- npm-cache.com
- pypi-get.com
- js-mirror.com
- eth-mainnet.nodereal.io
- go.getblock.io
- eth.llamarpc.com

url:
- https://npm-cache.com:443/router

sha256:
- 54dc7ea54a1317cca0e890a2770630cf7fa6c97813e0cb9d2caa93012b350668
- fd3ca4007b225fdf8de7af4345a19179d5efa8c4bb9205f88cda806e5684b1eb
- 9fc2570b7cef51c1b8df116d144d11ff4096357be7d2c4c6367cfc2509cf1bcc

sha1:
- 35a672cf34b996b91f3e1c28cbf3a05a37e036e4
- 686aa40d0fc22c8d569494543a0f891f359f2f99
- f525d52ceb966516686b482d3dc0137028cc6a63

email:
- claude@users.noreply.github.com

## Additional indicators (non-standard types)

file_artifact:
- /tmp/bun-dl-*/
- node_modules/keyv/Math_Symbol.js

user_agent:
- Bun/1.3.13

ethereum_contract:
- 0xE1f2395ee43e45A1556EC6438a88c31B83493103 (StringListStore; returns C2 domain; selector 0x53ed5143)

attribution_string:
- Shai-Hulud: Here We Go Again (description of attacker-controlled exfil GitHub repos)
- IfYouBlockThisAPIKeyItWillCrashTheLiveProductionServersOfAllThirdPartyClients
- thebeautifulmarchoftime (signed fallback marker)
- chore: update config (commit message used by worm)

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/chaindrop-worm-400-npm-two-billion/
- L2: https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack
- L2: https://www.microsoft.com/en-us/security/blog/2026/08/04/chaindrop-supply-chain-compromise-anatomy-self-propagating-worm/
- L2: https://www.wiz.io/blog/keyv-and-cacheable-npm-supply-chain-attack

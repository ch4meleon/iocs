# IOCs: ChainDrop npm supply chain attack (Shai-Hulud worm variant)

**Source:** https://www.securityweek.com/over-400-npm-packages-infected-in-chaindrop-supply-chain-attack/
**Date collected:** 2026-08-06

Over 2,200 malicious versions of 440+ npm packages were published in the ChainDrop
campaign (Mini Shai-Hulud variant). Malware: Bun-loaded credential stealer / worm
with EtherHiding (Ethereum) C2, self-propagation via stolen npm tokens and GitHub
credentials. Core indicators below from the Microsoft Security Blog, JFrog Security
Research, and StepSecurity analyses linked from the article.

ip_address:
- (none found)

domain:
- npm-cache.com
- pypi-get.com
- js-mirror.com

url:
- https://npm-cache.com:443/router

sha256:
- 54dc7ea54a1317cca0e890a2770630cf7fa6c97813e0cb9d2caa93012b350668
- 9fc2570b7cef51c1b8df116d144d11ff4096357be7d2c4c6367cfc2509cf1bcc
- fd3ca4007b225fdf8de7af4345a19179d5efa8c4bb9205f88cda806e5684b1eb

sha1:
- (none found)

md5:
- (none found)

email:
- (none found)

## Additional artifacts (context / hunting leads, not standard IOC types)

Ethereum C2 contract (EtherHiding):
- 0xE1f2395ee43e45A1556EC6438a88c31B83493103 (function selector 0x53ed5143)

Signed GitHub fallback markers (commit-message search strings):
- thebeautifulmarchoftime
- thebeautifulsnadsoftime

GitHub exfiltration marker (attacker-created public repo description):
- Shai-Hulud: Here We Go Again

Malicious file names (preinstall loader / second stage):
- setup.mjs
- Math_Symbol.js
- math_init.js
- Math_init.js
- math_<guid>.js

Persistence / repository hook files injected into GitHub branches:
- .claude/settings.json
- .claude/setup.mjs
- .claude/math_init.js
- .vscode/tasks.json
- .vscode/setup.mjs
- .github/workflows/codeql_analysis.yml
- format-results.txt
- branch: dependabot/github_actions/format/setup-formatter

Compromised GitHub repositories (initial compromise):
- github.com/jaredwray/keyv
- github.com/jaredwray/cacheable
- github.com/jaredwray/ecto

Malicious commit SHAs (GitHub, abbreviated; full SHA for keyv release commit):
- ee2681a (keyv "release: v6.0.0")
- d8c850c (keyv "chore: update config" hooks)
- f97eabc (keyv "remove preinstall test") -> f97eabcdd0571051f1fce3f05d6c029dac3f2ac78
- 1f79edd (keyv monorepo payload commit)
- 893f73f (cacheable setup-files-v1)
- 983ce1a (ecto release v5.0.1)

Malicious npm packages — 11 verified full worm carriers:
- keyv@6.0.0
- flat-cache@6.1.24
- file-entry-cache@11.1.6
- cacheable-request@13.0.20
- @cacheable/utils@2.5.1
- cacheable@2.5.1
- @cacheable/memory@2.2.1
- cache-manager@7.2.10
- @cacheable/node-cache@3.1.2
- ecto@5.0.1
- @cacheable/net@2.1.1

Plus 433 additional worm-propagated packages (2,201 versions), including
@keyv/* 6.0.0 adapters, @servicetitan (141), @onereach (78), @or-sdk (74),
@ornikar (42), @qlik (28), @nebula.js (22), @arv-bedrock, @deliveroo, @picsart,
@adminide-stack, @hubsync, @thiennq, @umacloud, @workbench-stack and 26 unscoped
packages. Full enumerable list: StepSecurity OSS Security Feed and JFrog research post
(https://research.jfrog.com/post/shai-hulud-is-back-august/).

## Pages visited

- L1: https://www.securityweek.com/over-400-npm-packages-infected-in-chaindrop-supply-chain-attack/ (no IOCs; aggregator)
- L2: https://www.microsoft.com/en-us/security/blog/2026/08/04/chaindrop-supply-chain-compromise-anatomy-self-propagating-worm/
- L2: https://research.jfrog.com/post/shai-hulud-is-back-august/
- L2: https://www.stepsecurity.io/blog/chaindrop-npm-worm
- L2: https://socket.dev/blog/popular-npm-packages-in-the-keyv-and-cacheable-namespaces-compromised-in-active-supply-chain (no IOCs — blocked by Cloudflare bot check)
- L3: https://app.stepsecurity.io/oss-security-feed (no IOCs — requires authentication)

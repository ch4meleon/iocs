# IOCs: Open VSX Evil Twin Extensions + Related Shai-Hulud npm/PyPI Campaigns

**Source:** https://thehackernews.com/2026/08/open-vsx-removes-77-malicious-evil-twin.html
**Date collected:** 2026-08-05

ip_address:
- 83.142.209.194

domain:
- mangorbit.com
- filev2.getsession.org
- api.masscan.cloud
- git-tanstack.com
- zero.masscan.cloud

url:
- https://git-tanstack.com/transformers.pyz
- https://zero.masscan.cloud/v1/telemetry

sha256:
(none)

sha1:
(none)

md5:
(none)

email:
- claude@users.noreply.github.com

## Additional indicators (campaign artifacts)

extension_id (malicious Open VSX "evil twin" extensions, L1):
- amd.gaia-vscode
- artsy.artsy-studio-extension-pack
- configcat.configcat-feature-flags
- iotaledger.iota-move
- marketplace.visualstudio
- obyte.oscript-vscode-plugin
- openeuphoria.vscode-euphoria
- oss.sfmc-devtools-vscode
- rumbledb.jsoniq-vscode
- ssagov.uef-snippets
- taskfile.vscode-task
- doi.fileheadercomment
- mengsiCode.vscode-django-boilerplate
- move.move-analyzer
- uavcan.dsdl
- vs-publisher-988541.apexsql-power-tools
- casualjim.gotemplate
- jcamp.dotnet-test-provider-view
- superposition.supertoml-analyzer

package (poisoned npm/PyPI artifacts, related ChainDrop / Mini Shai-Hulud campaigns):
- keyv@6.0.0
- flat-cache@6.1.23
- cache-manager@7.2.9
- guardrails-ai@0.10.1
- mistralai@2.4.6
- @opensearch-project/opensearch@3.5.3, 3.6.2, 3.7.0, 3.8.0
- @squawk/mcp@0.9.5
- @squawk/weather@0.5.10
- @squawk/flightplan@0.5.6
- @tallyui/connector-medusa@1.0.1, 1.0.2, 1.0.3
- @tallyui/connector-vendure@1.0.1, 1.0.2, 1.0.3
- lightning@2.6.2, 2.6.3
- intercom-client@7.0.4
- intercom/intercom-php@5.0.2

## Notes

- `mangorbit[.]com` (defanged in article) normalized to `mangorbit.com` — the shared data-exfiltration domain for all 77 Open VSX extensions; registered 2026-07-15, 11 days before first packages were published.
- Malicious payload filenames observed: `extension.js` (Open VSX), `router_init.js`, `setup.mjs`, `Math_Symbol.js`, `start.py`, `router_runtime.js`, `setup-intercom.sh`, `transformers.pyz`.
- `claude@users.noreply.github.com` is the hardcoded author identity used by Mini Shai-Hulud for GitHub-based exfiltration commits (impersonating Claude Code), not a victim address.
- Legitimate infrastructure abused by the malware (e.g., `api.github.com` token-validation endpoint, official GitHub releases for Bun runtime) was excluded from the IOC list.
- CVE-2026-45321 (TanStack supply chain compromise) referenced in related coverage.
- The primary source report (manifold.security/blog/open-vsx-evil-twin-extensions) was not crawled due to the same-domain crawl rule; additional hashes/C2 details may exist there.

## Pages visited

- L1: https://thehackernews.com/2026/08/open-vsx-removes-77-malicious-evil-twin.html
- L2: https://thehackernews.com/2026/08/keyv-linked-npm-worm-poisons-hundreds.html (no standard IOCs)
- L3: https://thehackernews.com/2026/05/mini-shai-hulud-worm-compromises.html
- L3: https://thehackernews.com/2026/04/pytorch-lightning-compromised-in-pypi.html

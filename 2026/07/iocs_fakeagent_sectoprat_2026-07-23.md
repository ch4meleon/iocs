# IOCs: FakeAgent Campaign — Fake Claude App via Bing Ads Pushes SectopRAT

**Source:** https://www.bleepingcomputer.com/news/security/fake-claude-app-promoted-by-bing-ads-pushes-sectoprat-malware/
**Date collected:** 2026-07-23

domain:
- claude.ai.download-app.us
- downloading-api.it.com

url:
- https://claude.ai/public/artifacts/ca456f1f-44c0-42af-b329-4f1c7534a877
- http://claude.ai.download-app.us
- http://downloading-api.it.com/html/claude/win

sha256:
- 25c043617523fa89b58f6acd5f4b66de42587093dcd2329721f6adbbc048720b
- 8dff14efa3c2b8a348c120f5739927c1668de05c3d91425e30b4e6a3ba776791
- b3e51746b31bf98aa30422a81f8f356ecaaa0f4e66a19637b6639c05575a3371

## Notes
- Ethereum contract used for EtherHiding C2: 0xc1907d7be91f95903ad66d775c397302e7dd9228
- SHA256 hashes sourced from Huntress researcher Tanner (@wbmmfq) X thread referencing the same malware campaign
- Malicious Claude Artifact UUID: ca456f1f-44c0-42af-b329-4f1c7534a877 (taken down by Anthropic on July 22, 2026)
- Malware files: ClaudeDesktop.exe / DockerDesktop.exe (legit signed binaries used for DLL sideloading), libcef.dll (malicious sideloaded DLL), tempdir.dll, sslconf.exe, cache.dat, appcfg.dat

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/fake-claude-app-promoted-by-bing-ads-pushes-sectoprat-malware/ (no IOCs)
- L2: https://www.huntress.com/blog/fakeagent-claude-desktop-malvertising-ends-in-dotnet-rat
- L3: https://x.com/wbmmfq/status/2049895200575922373

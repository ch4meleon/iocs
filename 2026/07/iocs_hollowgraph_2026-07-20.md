# IOCs: HollowGraph Malware

**Source:** https://thehackernews.com/2026/07/hollowgraph-malware-hides-c2-and-stolen.html
**Date collected:** 2026-07-20

## Indicator Summary

HollowGraph is a .NET DLL implant that abuses Microsoft Graph API to use a compromised Microsoft 365 calendar as a covert command-and-control channel. It communicates via the attacker-controlled domain `cloudlanecdn.com` for DNS tunneling to refresh credentials, and stores configuration in `logAzure.txt`.

domain:
- cloudlanecdn.com

sha1:
- f1b2d650c5b7e4c598e808c727e867b71d27f4b3

## Pages visited

- L1: https://thehackernews.com/2026/07/hollowgraph-malware-hides-c2-and-stolen.html
- L2: https://www.group-ib.com/blog/hollowgraph-microsoft-365/ (no additional IOCs found beyond reported C2 domain)
- L3: https://tap.group-ib.com/malware/reports/f1b2d650c5b7e4c598e808c727e867b71d27f4b3 (authentication required - no IOCs extracted)
- L3: https://research.checkpoint.com/2026/cavern-manticore-exposing-iran-linked-modular-c2-framework/ (empty response - no IOCs extracted)

## Notes

- The Group-IB blog states "the full indicator set, including file hashes, is in Group-IB's report" but the detailed IOC list is behind the Group-IB Threat Intelligence Portal (TAP), which requires authentication.
- The SHA1 hash `f1b2d650c5b7e4c598e808c727e867b71d27f4b3` was extracted from the TAP portal URL path and represents a malware sample/report identifier.
- Additional artifacts mentioned but not classifiable as standard IOC types: `logAzure.txt` (config file), `File{n}.txt` (attachment naming pattern), calendar event date `2050-05-13`, and subject patterns (`Event ID: <taskID>`, `Boss{..}ID{..}`).

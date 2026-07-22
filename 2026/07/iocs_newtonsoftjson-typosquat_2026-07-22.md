# IOCs: Trojanized Newtonsoft.Json Fork Hides Game-Rigging Code

**Source:** https://thehackernews.com/2026/07/trojanized-newtonsoftjson-fork-hides.html
**Date collected:** 2026-07-22

ip_address:
- 185.126.237.64

url:
- https://www.nuget.org/packages/Newtonsoftt.Json.Net/

## Notes

- The C2/exfiltration server uses port 5341 on IP 185.126.237.64.
- The malicious package also uses an API key header: `X-Seq-ApiKey: theperfectheist2025`.
- Seven malicious package versions were published: 11.0.4, 11.0.5, 11.0.7, 11.0.8, 11.0.9, 11.0.10, 11.0.11.
- The NuGet publisher account was `MagicalPuff96`.
- Original research by JFrog at: https://jfrog.com/blog/nuget-typosquat-targets-betting-platform/

## Pages visited

- L1: https://thehackernews.com/2026/07/trojanized-newtonsoftjson-fork-hides.html

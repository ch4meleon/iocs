# IOCs: Fake Notepad++ Plugin Delivers MATCHBOIL.V2 in UAC-0099 Attacks

**Source:** https://thehackernews.com/2026/07/fake-notepad-plugin-delivers.html
**Date collected:** 2026-07-24

ip_address:
- (none found)

domain:
- easysend.co

url:
- (none found - phishing URLs use link shorteners, no specific URLs disclosed)

sha256:
- (none found)

sha1:
- (none found)

md5:
- (none found)

email:
- (none found)

## Pages visited

- L1: https://thehackernews.com/2026/07/fake-notepad-plugin-delivers.html (IOCs: easysend.co)
- L2: https://thehackernews.com/2025/08/cert-ua-warns-of-hta-delivered-c.html (no IOCs)
- L2: https://thehackernews.com/2023/12/uac-0099-using-winrar-exploit-to-target.html (no IOCs)

## Notes

The Hacker News article is a summary of a CERT-UA advisory (https://cert.gov.ua/article/6318634) and does not publish the raw technical indicators (hashes, IP addresses) in the article body. The only domain IOC explicitly referenced is **easysend.co** (a file-sharing service abused to host malicious ZIP archives).

### Malware / Tooling identified in article (for context, not IOCs per se)

| Component | Description |
|---|---|
| NppExport.dll (LUNCHPOKE) | Malicious Notepad++ plugin DLL |
| updater.rar | Password-protected archive delivered by LUNCHPOKE |
| RemoteLibUpdater.exe (BURNYBEAR) | Loader that decompresses InitTest.dll |
| InitTest.dll (MATCHBOIL.V2) | Modified C#-based MATCHBOIL loader |
| MATCHBOIL | C# loader (previous version) |
| MATCHWOK | C# backdoor |
| DRAGSTARE | C# stealer |
| LONEPAGE | VBS malware (earlier campaigns) |

### CVEs referenced

- CVE-2023-38831 (WinRAR)
- CVE-2025-66376 (Zimbra)
- CVE-2026-8496 (SOGo Webmail)
- CVE-2025-49113 (Roundcube)

### Threat Actors

- UAC-0099 (Russia-aligned, primary in this article)
- Laundry Bear / CL-STA-1114 / TA488 / UNK_PitStop / Void Blizzard (mentioned in related disclosure)
- TA458 (Operation RoundPress)
- APT28 / TA422 (mentioned for context)

# IOCs: Targeted Attack on Government Entities in the Middle East | Part 1

**Source:** https://www.zscaler.com/blogs/security-research/targeted-attack-government-entities-middle-east-part-1
**Date collected:** 2026-07-20

## Indicators of Compromise

### domain
- api.telegram.org

### url
- https://api.telegram.org/bot[BOT_TOKEN]/getUpdates?offset=[N]

### md5
- ----WebKitFormBoundary7MA4YWxkTrZu0g

**Note:** The above string is a mutex name used by TELESHIM to ensure single-instance execution.

### File Paths (for detection/sigma rules)
- C:\programdata\shimgen_Data\
- C:\programdata\shimgen_Data\shimgen.exe
- C:\programdata\shimgen_Data\AsTaskSched.dll
- %TEMP%\CVR9EEA.tmp

### Filenames
- RegSchdTask.exe
- AsTaskSched.dll
- shimgen.exe

### Scheduled Task
- shimgen

### User-Agent
- Mozilla/5.0 (Macintosh; Intel Mac OS X 10_5_8) AppleWebKit/534.31 (KHTML, like Gecko) Chrome/13.0.748.0 Safari/534.31

### XOR Decryption Key (44-byte, hex)
- 8F380CDA296F34DE27697A1A53051849B69D59E528D7E669F17CF8D3CF220B6696DA776534401C8A0F0C31C6

### WMI Query
- wmic memorychip get speed

## Malware Families
- TELESHIM (32-bit C++ Windows DLL, Telegram C2 backdoor)
- MIXEDKEY (64-bit Windows Loader)
- BINDCLOAK (C2 implant, detailed in Part 2)

## Threat Actor
- East Asia-linked threat actor targeting government entities in the Middle East

## Pages visited

- L1: https://www.zscaler.com/blogs/security-research/targeted-attack-government-entities-middle-east-part-1 (IOC table at bottom of page truncated due to page size; SHA256 hashes for malware samples could not be extracted)
- L2: https://threatlibrary.zscaler.com/threats/329bd2ab-0c8e-4368-9811-827e5ce02426 (Win32.Backdoor.TELESHIM - no additional IOCs)
- L2: https://threatlibrary.zscaler.com/threats/d047d77c-b9ed-459d-90e1-47e9b6f65dfb (Win64.Loader.MIXEDKEY - no additional IOCs)

## Notes
- The article's dedicated IOC table (likely containing SHA256 hashes for TELESHIM and MIXEDKEY samples) was truncated during extraction due to the excessive navigation boilerplate on the Zscaler website. The main article content was extracted before truncation occurred at the "Post-compromise activity" section.
- Part 2 of this blog post (BINDCLOAK analysis) may contain additional IOCs.

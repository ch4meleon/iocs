# IOCs: TELESHIM / MIXEDKEY / BINDCLOAK — Telegram C2 Campaign Against Middle East Governments

**Source:** https://thehackernews.com/2026/07/teleshim-abuses-telegram-for-c2-in.html
**Date collected:** 2026-07-27

domain:
- cert.hypersnet.com

md5:
- C99F29AC08454855B3D538960BB2F34F

## Additional artifacts (non-standard IOC types)

Mutex:
- ----WebKitFormBoundary7MA4YWxkTrZu0g

User-Agent:
- Mozilla/5.0 (Macintosh; Intel Mac OS X 10_5_8) AppleWebKit/534.31 (KHTML, like Gecko) Chrome/13.0.748.0 Safari/534.31

XOR key (44-byte rolling):
- 8F380CDA296F34DE27697A1A53051849B69D59E528D7E669F17CF8D3CF220B6696DA776534401C8A0F0C31C6

Scheduled task name:
- shimgen

Malware file paths:
- C:\programdata\shimgen_Data\
- C:\programdata\shimgen_Data\shimgen.exe
- C:\programdata\shimgen_Data\AsTaskSched.dll
- %TEMP%\CVR9EEA.tmp

## Notes
- The C2 domain cert.hypersnet.com was defanged as cert.hypersnet[.]com in the article (brackets removed).
- Hash C99F29AC08454855B3D538960BB2F34F appears as part of the filename "C99F29AC08454855B3D538960BB2F34F.PCPKEY" — a BINDCLOAK payload encrypted with environmental keying.
- TELESHIM abuses api.telegram.org (legitimate Telegram API) for C2, making API tokens/chat IDs ephemeral per-instance.
- The threat actor is assessed with moderate-to-high confidence as East Asian origin; not yet tied to a named group.
- Post-compromise activity observed July 7–9, 2026, mainly 7–11 a.m. UTC.

## Pages visited

- L1: https://thehackernews.com/2026/07/teleshim-abuses-telegram-for-c2-in.html
- L2: https://www.zscaler.com/blogs/security-research/targeted-attack-government-entities-middle-east-part-1 (IOCs section truncated by page size limit)
- L3: https://threatlibrary.zscaler.com/threats/329bd2ab-0c8e-4368-9811-827e5ce02426 (no IOCs — login-gated page)
- L3: https://threatlibrary.zscaler.com/threats/d047d77c-b9ed-459d-90e1-47e9b6f65dfb (no IOCs — login-gated page)

# IOCs: Operation Double Barrel (Joint Cybersecurity Advisory)

**Source:** https://asec.ahnlab.com/en/94696/
**Date collected:** 2026-07-30
**Campaign:** Operation Double Barrel — relationship between a state-sponsored threat actor and the Gunra ransomware group

## Summary

The IOCs for this report are **not publicly available on the webpage**. The article states:

> *"Gain access to related IOCs and detailed analysis by subscribing to AhnLab TIP."*

The page header indicates the following IOC sections exist in the full (subscription-gated) report:
- **File Hashes (MD5)**
- **Related Domains, URLs, and IP Addresses**

Additionally, two PDF reports (English and Korean) are linked from the page but could not be rendered/parsed by the crawler:

- https://image.ahnlab.com/atip/content/file/20260730/[AhnLab]Operation%20Double%20Barrel(ENG)(2026.07.30).pdf
- https://image.ahnlab.com/atip/content/file/20260730/[AhnLab]Operation%20Double%20Barrel(KOR)(2026.07.30).pdf

The PDFs are hosted behind AhnLab's content delivery infrastructure and likely contain the full IOCs.

## Contextual Indicators (from page content)

The following malware families, tools, and artifacts are mentioned in the report summary. While not extractable as standard IOCs, they provide threat-hunting context:

**Malware:**
- Struggle (SIGNBT 3.0) — backdoor
- Brandoor (COPPERHEDGE) — backdoor
- Gunra Ransomware

**Tools/Techniques observed:**
- Certipy, HookShot, Impacket, PsExec, Plink, Socat, Nircmd, OpenSSH
- PetitPotam (privilege escalation)
- UACBypass / UACMe
- FileZilla, WinSCP, TightVNC, Whale
- Webshell, WateringHole, SpearPhishing
- SupplyChain (watering hole via website development/management company)
- GitHub, Tistory (tistory.com — Korean blogging platform, possibly abused)

**Vulnerabilities exploited:**
- Financial Security Software A
- Financial Security Software I

## Pages visited

- L1: https://asec.ahnlab.com/en/94696/ (no IOCs — gated behind AhnLab TIP subscription)
- L2: https://asec.ahnlab.com/en/94704/ (no IOCs related to Operation Double Barrel — separate AtlasRAT article)
- L2: https://asec.ahnlab.com/ko/94696/ (no IOCs — Korean version, same gated content)
- L2: https://atip.ahnlab.com/ (no IOCs — AhnLab TIP marketing page, login required for data access)

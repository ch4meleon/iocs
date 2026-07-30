# IOCs: Minnesota Water Utilities Coordinated OT Attack & Related Iranian CyberAv3ngers Activity

**Source:** https://www.bleepingcomputer.com/news/security/hackers-target-over-30-minnesota-water-utilities-in-coordinated-ot-attack/
**Date collected:** 2026-07-29

## Summary

The primary article reports a coordinated cyberattack on over 30 Minnesota community water systems (July 26-27, 2026) targeting operational technology (OT). The threat actor behind this specific incident **remains unknown**, and no specific IOCs were published in the article or the associated MNIT advisory.

However, related articles reference Iranian-affiliated APT actors (CyberAv3ngers) who have previously targeted water utility PLCs. The following IOCs are from the CISA joint advisory AA23-335A (December 2023) STIX file, associated with the IRGC-affiliated CyberAv3ngers group that has targeted US water/wastewater facilities using Unitronics PLCs. The April 2026 joint advisory (IC3/2026/260407) additionally warns of Iranian hackers targeting Rockwell Automation/Allen-Bradley PLCs in critical infrastructure including water systems.

**Note:** The CISA advisory notes these IOCs are from December 2023 and may not reflect current activity. No specific IOCs for the July 2026 Minnesota attack have been publicly released as of this report.

ip_address:
- 178.162.227.180
- 185.162.235.206

sha256:
- 440B5385D3838E3F6BC21220CAA83B65CD5F3618DAEA676F271C3671650CE9A3

sha1:
- 66AE21571FAEE1E258549078144325DC9DD60303

md5:
- BA284A4B508A7ABD8070A427386E93E0

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/hackers-target-over-30-minnesota-water-utilities-in-coordinated-ot-attack/ (no IOCs — incident description only)
- L2: https://www.bleepingcomputer.com/news/security/us-warns-of-iranian-hackers-targeting-critical-infrastructure/ (no IOCs in article text — references joint advisory)
- L2: https://www.bleepingcomputer.com/news/security/cisa-shares-advice-on-isolating-vital-systems-during-cyberattacks/ (no IOCs — CISA guidance article)
- L2: https://mn.gov/mnit/media/blog/?id=38-761869 (no IOCs — MNIT incident response press release)
- L3: https://www.cisa.gov/news-events/cybersecurity-advisories/aa23-335a (advisory page — no IOCs in rendered page; IOCs from linked STIX file)
- L3: https://www.cisa.gov/sites/default/files/2023-12/AA23-335A.stix__0.xml (STIX XML — yielded IPs and hashes listed above)

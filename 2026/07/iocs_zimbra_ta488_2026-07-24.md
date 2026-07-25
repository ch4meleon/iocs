# IOCs: TA488 / ZimReaper Campaign — Zimbra Zero-Day (CVE-2025-66376)

**Source:** https://hackread.com/russian-hackers-zimbra-0-day-steal-emails-link-clicks/  
**Date collected:** 2026-07-24

## Key Context

- **CVE:** CVE-2025-66376 (stored XSS in Zimbra Collaboration Suite)
- **Threat Actor:** TA488 / Void Blizzard / Laundry Bear (Russia-aligned)
- **Malware:** ZimReaper (JavaScript browser stealer)
- **Persistence:** Application password named "ZimbraWeb" created via Zimbra API

---

domain:
- zmailanalytics.com
- zimbra-metadata.com
- analyticemailmeter.com
- emailanalytics.com.ua
- mailnalysis.com
- zimbrastat.com
- zimbrasoft.com.ua
- synacorzimbra.nl
- istc-cloud.com
- js-l1wt597cimk.i.zimbrasoft.com.ua
- js-26tik3egye4.i.zimbrasoft.com.ua

email:
- c.laurent.ejfa@proton.me
- j.moreau.epsc@proton.me
- liberty.insights@proton.me

sha256:
- 98df604ecc57f884a2e6ce3266a0013ad64455cac48442c2312cfa4765007aaf
- 60db9abae75cd8ccc49dd7ea5feb41677566dcd442f12ebc5745ffd2810fb874
- b1f5beb1175fc5c7d1806a2f0d900eb124c54f0286c5c52b66eea7a6633adb1d

md5:
- c010f64080b0b0997b362a8e6b9c618e

## Pages visited

- L1: https://hackread.com/russian-hackers-zimbra-0-day-steal-emails-link-clicks/ (no IOCs)
- L2: https://hackread.com/zimbra-email-platform-vulnerability-phishing-scam/ (no IOCs — unrelated 2023 article)
- L2: https://media.defense.gov/2026/Jul/22/2003965244/-1/-1/1/CSA_RUSSIA_PHISHING_TARGET_ZIMBRA.PDF (no IOCs — PDF not renderable by tool)
- L2: https://www.proofpoint.com/us/blog/threat-insight/ta488-targets-zimbra-mailservers-half-click-exploits (IOCs found)
- L3: https://www.seqrite.com/blog/operation-ghostmail-zimbra-xss-russian-apt-ukraine/ (IOCs found)

# IOCs: Laundry Bear / TA488 / Void Blizzard — Zimbra CVE-2025-66376 Campaign

**Source:** https://www.darkreading.com/cyberattacks-data-breaches/russian-hackers-zimbra-zero-day-us-ukraine-targets
**Date collected:** 2026-07-24

## Summary

Russian state-sponsored threat actor Laundry Bear (TA488 / Void Blizzard) exploited CVE-2025-66376, a stored XSS vulnerability in Zimbra Collaboration Suite (ZCS), to target Ukrainian government entities and US government, defense, and scientific organizations. The "half-click" phishing campaign required only opening/previewing a malicious email in Zimbra Webmail. The embedded JavaScript payload ("ZimReaper") exfiltrates credentials, session tokens, 2FA codes, and 90 days of email via DNS tunneling and HTTPS to actor-controlled C2 infrastructure.

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

sha256:
- 98df604ecc57f884a2e6ce3266a0013ad64455cac48442c2312cfa4765007aaf
- 60db9abae75cd8ccc49dd7ea5feb41677566dcd442f12ebc5745ffd2810fb874
- b1f5beb1175fc5c7d1806a2f0d900eb124c54f0286c5c52b66eea7a6633adb1d

md5:
- c010f64080b0b0997b362a8e6b9c618e

email:
- c.laurent.ejfa@proton.me
- j.moreau.epsc@proton.me
- liberty.insights@proton.me

## Pages visited

- L1: https://www.darkreading.com/cyberattacks-data-breaches/russian-hackers-zimbra-zero-day-us-ukraine-targets (no IOCs)
- L2: https://www.seqrite.com/blog/operation-ghostmail-zimbra-xss-russian-apt-ukraine/
- L2: https://www.proofpoint.com/us/blog/threat-insight/ta488-targets-zimbra-mailservers-half-click-exploits
- L2: https://www.ic3.gov/CSA/2026/260723.pdf (no IOCs — PDF could not be parsed as text)
- L3: https://media.defense.gov/2026/Jul/22/2003965244/-1/-1/1/CSA_RUSSIA_PHISHING_TARGET_ZIMBRA.PDF (no IOCs — PDF could not be parsed as text)

# IOCs: Fake Bank of America Phishing Scam (ScreenConnect RMM)

**Source:** https://www.infosecurity-magazine.com/news/fake-bank-of-america-phishing-scam/
**Date collected:** 2026-08-06

ip_address:
- 217.60.195.167

domain:
- bkofamerica.com
- kleinschnitg.com
- sectioncompil.com
- uploadtourl.com

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/fake-bank-of-america-phishing-scam/

## Notes

- 217.60.195.167: suspected C2 server for the ScreenConnect RMM payload, contacted over TCP port 8041; geolocates to the United Arab Emirates and is reportedly shared by other malware families (per Huntress).
- bkofamerica.com: phishing domain impersonating Bank of America (emails did not point to the legitimate domain).
- kleinschnitg.com: destination of the link in the phishing email (fake "Security Centre").
- sectioncompil.com: page from which the malicious zip (AccountGuardSetup.zip) originated.
- uploadtourl.com: file-sharing host used to stage the 17MB Base64-encoded ScreenConnect MSI installer (legitimate service abused).
- Malware artifacts (not standard IOC types): AccountGuardSetup.zip -> AccountGuardSetup.vbs -> ScreenConnect RMM disguised as a service named "Windows Security"; UAC bypass via ICMLuaUtil COM interface; no payload for macOS targets (they were instead prompted for personal information).
- No file hashes or email addresses were disclosed in the article.
- Original Huntress analysis (off-domain, not crawled per same-domain rule): https://www.huntress.com/blog/bank-spam-rmm

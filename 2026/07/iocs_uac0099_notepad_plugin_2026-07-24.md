# IOCs: UAC-0099 Fake Notepad++ Plugin Campaign Targeting Ukrainian Organizations

**Source:** https://securityaffairs.com/195923/cyber-warfare-2/uac-0099-is-now-hiding-malware-inside-a-fake-notepad-plugin-to-target-ukrainian-organizations.html
**Date collected:** 2026-07-24

## Notes

This article is a descriptive news write-up about the UAC-0099 campaign. The raw technical IOCs (file hashes, C2 IPs/domains) are not published in the article itself — they reside in the source CERT-UA advisory (linked below). Below are the indicators that could be extracted from the article text.

---

domain:
- easysend.co

url:
- https://cert.gov.ua/article/6318634

email:
- pierluigi.paganini@securityaffairs.co

## Contextual Indicators (not standard IOC types, but useful for detection)

**CVE:**
- CVE-2025-66376 (Zimbra "half-click" exploit used by related Laundry Bear campaign)

**Malware names referenced:**
- LUNCHPOKE (malicious NppExport.dll)
- BURNYBEAR (RemoteLibUpdater.exe)
- MATCHBOIL / MATCHBOIL.V2 (InitTest.dll)
- LONEPAGE
- DRAGSTARE

**File paths / artifacts:**
- %PUBLIC%\Libraries\fFthY3-Ytrevc3w-ab3\ (variable directory name)
- %PUBLIC%\Wallpapers\Background.exe (copied schtasks.exe)
- \W1n3r-U09oTy-Ap5\Updates (scheduled task name)
- /plugins/NppExport/NppExport.dll (plugin path)
- Evernote.zip (second-stage archive)
- updater.rar (password-protected archive)

## Pages visited

- L1: https://securityaffairs.com/195923/cyber-warfare-2/uac-0099-is-now-hiding-malware-inside-a-fake-notepad-plugin-to-target-ukrainian-organizations.html

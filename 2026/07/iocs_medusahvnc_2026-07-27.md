# IOCs: MedusaHVNC Malware

**Source:** https://www.securityweek.com/medusahvnc-malware-uses-hidden-windows-desktops-to-evade-detection/ (via BlackFog analysis at https://www.blackfog.com/medusahvnc-a-hidden-desktop/)
**Date collected:** 2026-07-27

ip_address:
- 51.89.204.28

domain:
- (none identified)

url:
- (none identified)

sha256:
- (hashes redacted by original researchers in published article)

sha1:
- (hashes redacted by original researchers in published article)

md5:
- (hashes redacted by original researchers in published article)

email:
- (none identified)

## Additional artifacts (file names observed during infection chain)

These are not cryptographic hashes but are file/directory names dropped by the malware that can serve as detection indicators:

- eepcxlhgdz.exe (AutoIt interpreter dropped under %TEMP%\Nx2981Okkr2\)
- zorsxklxfehdoals (encrypted payload dropped under %TEMP%\Nx2981Okkr2\)
- AFLlvOscPj.bat (persistence batch file placed in Startup folder)
- %TEMP%\Nx2981Okkr2\ (working directory where payloads are staged)
- C2 port: 4444
- XOR decryption key: 0xAE (single-byte)

## Pages visited

- L1: https://www.securityweek.com/medusahvnc-malware-uses-hidden-windows-desktops-to-evade-detection/ (1 IOC: IP address)
- L2: https://www.blackfog.com/medusahvnc-a-hidden-desktop/ (additional file-name artifacts; hashes redacted in published analysis)
- L3: https://www.blackfog.com/threats/ (no IOCs — index page)
- L3: https://www.blackfog.com/exploits/ (no IOCs — index page)

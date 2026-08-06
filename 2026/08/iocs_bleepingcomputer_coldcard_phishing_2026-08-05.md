# IOCs: COLDCARD security audit phishing attack (ScreenConnect RAT)

**Source:** https://www.bleepingcomputer.com/news/security/coldcard-security-audit-phishing-attack-installs-remote-access-tool/
**Date collected:** 2026-08-05

domain:
- activeretirementrelocation.com
- coldcardcompliance.com

sha256:
- 7ad243cd358d916e029ba8ff9a616dfdcab29b594a9ebf08a66a1c4bd63fb7e2
- 5f0dc835d9e37318f862c64db85cc094059bb5404a1c1752facdfd16a784570a

email:
- compliance@coldcardteamnews.com

## Notes

- `activeretirementrelocation.com` was defanged as `activeretirementrelocation[.]com` in the article; it is the ScreenConnect C2 server used by the threat actor.
- `7ad243cd...fb7e2` = SHA256 of `setup.msi` (ConnectWise ScreenConnect installer).
- `5f0dc835...4570a` = SHA256 of `docusign.exe` (legitimate signed decoy binary).
- Associated artifacts (not IOC types in this report): `Coldcard_Diagnostic_Tool.bat` (25.7 MB dropper downloaded from a GitHub account), `setup.msi`, `docusign.exe`.
- Phishing emails sent from `compliance@coldcardteamnews.com`, subject "Hardware audit now available"; fake portal at `coldcardcompliance.com`.
- No IPv4/IPv6, URL, SHA1, or MD5 indicators were present in the source pages.

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/coldcard-security-audit-phishing-attack-installs-remote-access-tool/
- L2: https://www.bleepingcomputer.com/news/security/coldcard-wallet-rng-flaw-likely-linked-to-88-million-bitcoin-theft/ (no IOCs)

# IOCs: MedusaHVNC Trojan

**Source:** https://securityaffairs.com/196111/malware/medusahvnc-trojan-creates-hidden-desktops-to-hijack-browsers-and-steal-data.html
**Date collected:** 2026-07-27

ip_address:
- 51.89.204.28

## Pages visited

- L1: https://securityaffairs.com/196111/malware/medusahvnc-trojan-creates-hidden-desktops-to-hijack-browsers-and-steal-data.html
- L2: https://www.blackfog.com/medusahvnc-a-hidden-desktop/ (no IOCs beyond those already collected at L1)

## Notes

- The C2 server **51.89.204.28** is hard-coded in the MedusaHVNC binary on TCP port **4444**.
- The BlackFog research article references "the hashes in the IOC table" but those hashes (MD5/SHA1/SHA256) were presented in an embedded image that could not be extracted via text rendering. The original BlackFog report at https://www.blackfog.com/medusahvnc-a-hidden-desktop/ contains this IOC table in image format.
- Additional technical details from the analysis: XOR key 0xAE (single-byte), ChaCha20 with 32-byte key and 12-byte nonce used for payload decryption.

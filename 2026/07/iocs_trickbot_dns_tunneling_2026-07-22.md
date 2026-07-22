# IOCs: TrickBot DNS Tunneling C2 Variant

**Source:** Infosecurity Magazine article + FortiGuard Labs research report
**Date collected:** 2026-07-22

## domain
- westurn.in

## Notes

- The **C2 domain** `westurn.in` was identified as the hardcoded domain used by this TrickBot variant for DNS tunneling C2 communications. The original C2 server was reported as shut down at the time of FortiGuard's analysis.
- **Campaign name:** `anchor_dns` – used in C2 command paths.
- **DNS resolver used:** `8.8.8.8` (Google Public DNS – legitimate service used by the malware, not an IOC).
- **Malicious DLL module:** `tcp469A.dll` – a downloaded module executed via rundll32.exe.
- **XOR encryption key:** `0xB9` – used for single-byte XOR encryption of C2 command data.
- **Detected as (AV signature):** `W64/TrickBot.WC!tr`
- **IPS signature:** `Trick.Botnet`

**Note on truncated content:** The IOCs section at the bottom of the Fortinet blog post (which likely contains sample SHA-256 hashes and the Appendix with API hash lists) was truncated due to page size limits and could not be fully retrieved. The domain `westurn.in` is the primary confirmed IOC from the available text.

## Pages visited

- L1: https://www.infosecurity-magazine.com/news/trickbot-dns-tunneling-c2/ (no IOCs – news summary only)
- L2: https://www.fortinet.com/blog/threat-research/inside-a-trickbot-variant-using-dns-tunneling-for-c2

# IOCs: Kali365 Microsoft Device Login Phishing (HackRead)

**Source:** https://hackread.com/kali365-exploit-microsoft-device-login-access-us-data/
**Date collected:** 2026-08-06

domain:
- api.ipify.org
- jellyfish.systems
- securedsnmail.com
- suitecorporate.com
- suitetosecured.com

## Pages visited

- L1: https://hackread.com/kali365-exploit-microsoft-device-login-access-us-data/ (no IOCs)
- L2: https://hackread.com/fbi-kali365-phishing-service-microsoft-365-account/ (no IOCs)
- L2: https://hackread.com/new-fishxproxy-phishing-kit-script-kiddies/ (no IOCs)
- L3: https://hackread.com/calphishing-eviltokens-kit-outlook-invites-m365/ (no IOCs)
- L3: https://hackread.com/bluekit-phishing-kit-targets-platforms-mfa-bypass-attack/ (no IOCs)
- L3: https://hackread.com/hackers-cloudflare-human-check-microsoft-365-phishing/ (IOCs found)

## Notes

- The Kali365-specific articles (L1, L2) contain no hard IOCs (no IPs, hashes, or malicious domains); they describe the device-code/OAuth token theft technique and reference a hunting query: threatName:"kali365" AND submissionCountry:"US" (ANY.RUN TI Lookup), plus FBI/CISA guidance at https://www.ic3.gov/PSA/2026/PSA260521.
- Concrete domains above were reported by DomainTools (L3 article) for a related Microsoft 365 phishing campaign abusing Cloudflare Turnstile; api.ipify.org is a legitimate IP-lookup API abused for victim geolocation (used by the kit, not attacker-owned).
- Cloudflare Turnstile static sitekey fingerprint associated with the campaign: 0x4AAAAAACG6TJhrsuZdpjsN (found across suitecorporate.com and suitetosecured.com).

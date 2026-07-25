# IOCs: Thailand Ministry of Finance – Hermes AI Agent & Hades Implant

**Source:** https://securityaffairs.com/195941/hacking/thailands-ministry-of-finance-targeted-with-hermes-ai-agent-running-unattended-hades-implant-staged.html
**Secondary Source:** https://hunt.io/blog/thailand-ministry-finance-targeted-with-hermes-ai-agent
**Date collected:** 2026-07-24

## ip_address:
- 43.246.208.207
- 103.97.0.57
- 118.107.222.232
- 202.181.27.115

## domain:
- redhatupdating432.dnsrd.com
- hermes-agent.org

## url:
- https://hermes-agent.org/
- https://github.com/nousresearch/hermes-agent
- https://github.com/peass-ng/PEASS-ng/tree/master/linPEAS
- https://nvd.nist.gov/vuln/detail/CVE-2021-3156
- https://nvd.nist.gov/vuln/detail/CVE-2021-4034
- https://nvd.nist.gov/vuln/detail/CVE-2017-7269

## email:
- pierluigi.paganini@securityaffairs.co

## Pages visited

- L1: https://securityaffairs.com/195941/hacking/thailands-ministry-of-finance-targeted-with-hermes-ai-agent-running-unattended-hades-implant-staged.html
- L2: https://hunt.io/blog/thailand-ministry-finance-targeted-with-hermes-ai-agent (IoC section truncated, see notes)

## Notes

The Hunt.io report at L2 contains a dedicated **Indicators of Compromise** section with file hashes (MD5/SHA1/SHA256) for recovered Hades payloads, which could not be extracted due to page truncation on the HTML renderer. The full IoC table is available directly at the source URL.

### Known C2 infrastructure details (not pure IOCs but operationally relevant):

| Host | Role | Ports |
|---|---|---|
| 43.246.208.207 (AS132883 TOPIDC, Hong Kong) | Main staging server; ShadowPad host; Hades C2; VShell C2 | 80, 443, 8080, 8443, 19443, 21083 |
| 202.181.27.115 (Converged Communications Ltd, Hong Kong) | Hades C2 (Linux beacon) | 12443 |
| 118.107.222.232 (The Gigabit, Malaysia) | Related server (TLS cert pivot) | Unknown |
| 103.97.0.57 (AS133073 HK Kwaifong Group, Hong Kong) | Operator SSH access host | Unknown |

### Known C2 URI paths (Hades implant):
- `/assets/app.min.js` – check-in
- `/assets/vendor.js` – C2 tasking
- `/assets/main.js` – upload

### Known webshell deployment path:
- `/storage/Counter/nine/.journald-cache.php` (on MOF web server)

### Known Hades sample filenames:
- `dwm_33b7.exe` (Windows, beacons to 43.246.208.207:443)
- `multipathd_04d0` (Linux ELF, beacons to 202.181.27.115:12443)
- `hades_linux_amd64`, `hades_windows_amd64` (template names)
- `ctfmon`, `csrss`, `conhost`, `MicrosoftEdgeUpdate` (Windows masquerade names)
- `kworker`, `multipathd`, `accounts-daemon` (Linux masquerade names)

### JA4X TLS certificate fingerprint:
- `7d5dbb3783b4_7d5dbb3783b4_e1926048963f`

### Exploit CVEs staged:
- CVE-2021-4034 (PwnKit)
- CVE-2021-3156 (sudo heap overflow)
- CVE-2017-7269 (IIS 6.0 WebDAV buffer overflow)

# IOCs: Chaos ransomware / msaRAT

**Source:** https://securityaffairs.com/195876/malware/chaos-ransomware-deploys-browser-based-msarat-to-evade-network-detection.html
**Date collected:** 2026-07-23

ip_address:
- 172.86.126.18

domain:
- is-01-ast.ols-img-12.workers.dev
- stun2.l.google.com
- global.turn.twilio.com

url:
- http://172.86.126.18:443/update_ms.msi
- https://github.com/Cisco-Talos/IOCs/blob/main/2026/07/chaos-msarat.txt

email:
- pierluigi.paganini@securityaffairs.co

## Notes

- `stun2.l.google.com` is a legitimate Google STUN server abused by the malware for WebRTC NAT traversal.
- `global.turn.twilio.com` is Twilio's legitimate TURN relay service used by the malware to relay C2 traffic, making the attacker's real IP address invisible in network traffic.
- `is-01-ast.ols-img-12.workers.dev` is the attacker-controlled Cloudflare Workers endpoint used for WebRTC signaling (SDP Offer/Answer exchange).
- No file hashes (MD5/SHA1/SHA256) were published in the Cisco Talos GitHub IOCs file or in the articles.
- ClamAV signature: `Win.Downloader.ChaosRaas-10060321-0`
- Snort 2 SIDs: 1:66840, 1:66841, 1:66839
- Snort 3 SIDs: 1:301587, 1:66839
- Malicious file: `update_ms.msi` (impersonates Windows update), `lib.dll` (msaRAT payload)
- Binding names observed: `msaOpen`, `msaClose`, `msaError`, `msaMessage`, `dataAck`

## Pages visited

- L1: https://securityaffairs.com/195876/malware/chaos-ransomware-deploys-browser-based-msarat-to-evade-network-detection.html
- L2: https://github.com/Cisco-Talos/IOCs/blob/main/2026/07/chaos-msarat.txt
- L2: https://blog.talosintelligence.com/chaos-msarat-living-off-the-browser-to-build-covert-c2-channel/

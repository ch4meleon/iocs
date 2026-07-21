# IOCs: JadePuffer / EncForge Ransomware Campaign (AI model targeting)

**Source:** https://www.bleepingcomputer.com/news/security/jadepuffer-agentic-attacks-now-target-ai-model-data-with-ransomware/
**Date collected:** 2026-07-20

ip_address:
- 34.153.223.102
- 45.131.66.106
- 64.20.53.230

domain:
- proton.me

url:
- http://34.153.223.102:9191/lockd
- http://34.153.223.102:9191/.lockd
- hxxp://45.131.66.106:4444/beacon

sha256:
- 8cb0c223b018cecef1d990ec81c67b826eb3c30d54f06193cf69969e9a8baea2
- ea7822eac6cecef7746c606b862b4d3034856caf754c4cf69533662637905328

email:
- e78393397@proton.me

## Notes

- **34.153.223.102**: C2 server hosting the ENCFORGE (lockd) ransomware binary on port 9191.
- **45.131.66.106**: C2 beaconing infrastructure used by the cron persistence beacon (every 30 min).
- **64.20.53.230**: IP address referenced by the agentic operator as a backup destination during the destruction phase ("data already backed up to 64.20.53.230"). Inclusion uncertain but documented here for completeness.
- **8cb0c223b018cecef1d990ec81c67b826eb3c30d54f06193cf69969e9a8baea2**: SHA-256 of the UPX-packed ENCFORGE/lockd binary (1,501,888 bytes, UPX 5.20).
- **ea7822eac6cecef7746c606b862b4d3034856caf754c4cf69533662637905328**: SHA-256 of the unpacked ENCFORGE/lockd binary (4,767,896 bytes, Go 1.22.12 static).
- **e78393397@proton.me**: Extortion contact email embedded in the EncForge ransom note. Matches the contact from the prior JADEPUFFER campaign.
- Neither hash was detected by common threat intelligence tools at the time of analysis.
- The embedded RSA-2048 public key is a build-specific IOC (see below).

## Embedded RSA-2048 Public Key (binary IOC)

The following RSA-2048 public key is compiled into the ENCFORGE binary and is a durable, build-specific indicator:

```
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7wZB6Q/Y0wZ7/Gax8i3Z
PybS9t5fCkOT37mavrcSZ+V+tt6M6jChhf+b+ASUNa6uIr4l+MCc7XAsJmpmnyyd
2aZYhMSbbO5YpmKL6AFgJBhhB37NvpzWje6CFk5rpZQ7sUlhMHXdi63Bqo6bAZaW
8+MDG8K6W55Y10XmRTqKUPrDYJFD9z8LnbJJeBQggpM3XS0C0lXF5yxq0WpyMpnO
8O24t+jzhkRuCwVsMd7sw3qKxQ7t7fdBYs4wEvL9r/jrt2Z7OiBnueEIuJFDULjF
ckJshJGwNNjXiEmZr7mT9ei56UvIwPjnepQC6ex2PwnmcYw1uPef1A3Qpy+VhxyT
dwIDAQAB
-----END PUBLIC KEY-----
```

## Related CVEs (exploited by this threat actor)

- CVE-2025-3248 (Langflow unauthenticated RCE — initial access vector)
- CVE-2021-29441 (Nacos authentication bypass)

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/jadepuffer-agentic-attacks-now-target-ai-model-data-with-ransomware/ (no IOCs)
- L2: https://www.bleepingcomputer.com/news/security/jadepuffer-ransomware-used-ai-agent-to-automate-entire-attack/ (no IOCs)
- L2: http://www.sysdig.com/blog/jadepuffer-evolves-the-agentic-threat-actor-deploys-ransomware-built-to-destroy-ai-models (IOCs found)
- L2: https://www.sysdig.com/blog/jadepuffer-agentic-ransomware-for-automated-database-extortion (IOCs found)

# IOCs: Kimi K3 Agents Found Redis Zero-Days — PoC Repositories & Indicators

**Source:** https://thehackernews.com/2026/07/kimi-k3-agents-found-redis-zero-days.html
**Date collected:** 2026-07-24

## Summary

Bera Buddies (Kimi K3 AI agents) and Lyutoon discovered and published authenticated RCE PoCs for multiple Redis versions exploiting two vulnerability classes: a Streams shared-NACK double-free (CVE-2026-25243 patch bypass) and a RedisBloom TDigest/TopK out-of-bounds write. Redis shipped fixes on July 23, 2026.

---

sha256:
- aa049e689e141a4358ad1d4562dc49c88a89fbab711fd8fcc33f684c80b26301

url:
- https://github.com/berabuddies/redis-poc
- https://github.com/berabuddies/redis-poc/blob/main/A_exploit_stock.py
- https://github.com/berabuddies/redis-poc/blob/main/P74_exploit.py
- https://github.com/berabuddies/redis-poc/blob/main/P74_g2.py
- https://github.com/berabuddies/redis-poc/blob/main/P86_exploit.py
- https://github.com/berabuddies/redis-poc/blob/main/P88W_exploit.py
- https://github.com/berabuddies/redis-poc/blob/main/P88W_lib.py
- https://github.com/berabuddies/redis-poc/blob/main/P88W_corrupt.py
- https://github.com/berabuddies/redis-poc/blob/main/T88_exploit.py
- https://github.com/berabuddies/redis-poc/blob/main/A_lib.py
- https://github.com/berabuddies/redis-poc/blob/main/G2_arbread.py
- https://github.com/berabuddies/redis-poc/blob/main/HARDENING.md
- https://github.com/berabuddies/redis-poc/blob/main/calibrate.sh
- https://github.com/berabuddies/redis-poc/blob/main/crc64.c
- https://github.com/berabuddies/redis-poc/blob/main/crc64.h
- https://github.com/berabuddies/redis-poc/blob/main/crcspeed.c
- https://github.com/berabuddies/redis-poc/blob/main/crcspeed.h
- https://github.com/berabuddies/redis-poc/blob/main/P74_loop.sh
- https://github.com/berabuddies/redis-poc/blob/main/P86_run.sh
- https://github.com/Lyutoon/redis-RCE-poc
- https://github.com/Lyutoon/redis-RCE-poc/blob/main/exploit_chain_8.8.0.py
- https://github.com/Lyutoon/redis-RCE-poc/blob/main/redis_setup.sh
- https://github.com/redis/redis/releases
- https://github.com/redis/redis/releases/tag/8.6.4
- https://github.com/redis/redis/pull/15081
- https://github.com/redis/redis/blob/8.6.4/src/rdb.c
- https://github.com/redis/redis/blob/8.6.5/src/rdb.c
- https://github.com/RedisBloom/RedisBloom/pull/1038
- https://github.com/berabuddies
- https://x.com/Fried_rice/status/2080190071102460108
- https://x.com/Fried_rice/status/2080059356322918777
- https://nvd.nist.gov/vuln/detail/CVE-2026-25243
- https://nvd.nist.gov/vuln/detail/CVE-2026-25589
- https://www.cisa.gov/known-exploited-vulnerabilities-catalog

domain:
- github.com
- x.com
- nvd.nist.gov
- www.cisa.gov

## Pages visited

- L1: https://thehackernews.com/2026/07/kimi-k3-agents-found-redis-zero-days.html
- L2: https://github.com/berabuddies/redis-poc
- L2: https://github.com/Lyutoon/redis-RCE-poc
- L2: https://github.com/berabuddies/redis-poc/blob/main/README.md
- L2: https://github.com/Lyutoon/redis-RCE-poc/blob/main/README.md
- L2: https://github.com/berabuddies/redis-poc/blob/main/A_exploit_stock.py
- L2: https://github.com/berabuddies/redis-poc/blob/main/P86_exploit.py

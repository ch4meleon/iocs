# IOCs: JADEPUFFER Agentic Ransomware / ENCFORGE Payload

**Source:** News4Hackers article + Sysdig Threat Research Team (TRT) original reports
**Date collected:** 2026-07-22

ip_address:
- 34.153.223.102
- 45.131.66.106

domain:
- proton.me

url:
- http://34.153.223.102:9191/lockd
- http://34.153.223.102:9191/.lockd
- http://45.131.66.106:4444/beacon

sha256:
- 8cb0c223b018cecef1d990ec81c67b826eb3c30d54f06193cf69969e9a8baea2
- ea7822eac6cecef7746c606b862b4d3034856caf754c4cf69533662637905328

email:
- e78393397@proton.me

## Additional intelligence (not standard IOCs)

**CVE identifiers:**
- CVE-2025-3248 (Langflow /api/v1/validate/code missing authentication)
- CVE-2021-29441 (Nacos authentication bypass)

**Bitcoin address (ransom payment):**
- 3J98t1WpEZ73CNmQviecrnyiWrnqRhWNLy

**Embedded RSA-2048 public key (build-specific durable IOC):**
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

**Malware binary names:**
- ENCFORGE (deployed as `lockd` on target)
- keyforge (companion keygen tool)
- encfile (internal Go project name: encfile/cmd/lock)

**Encrypted file extension:** .locked

**Targeted AI/ML file extensions:** .ckpt, .h5, .onnx, .pb, .pkl, .pickle, .pt, .pt2, .pth, .safetensors, .ggml, .gguf, .model, .faiss, .arrow, .feather, .parquet, .tfrecord, .npy, .npz, .vec, .duckdb

**Internal Docker image used for escape:** registry.internal/app:2.3.1

## Pages visited

- L1: https://www.news4hackers.com/jadepuffer-agentic-ransomware-resurfaces-attacks-ai-assets-with-encforge-payload/
- L2: https://www.news4hackers.com/jadepuffer-returns-with-new-ransomware-targeting-ai-models-and-infrastructure/
- L3: https://sysdig.com/blog/jadepuffer-evolves-the-agentic-threat-actor-deploys-ransomware-built-to-destroy-ai-models
- L3: https://sysdig.com/blog/jadepuffer-agentic-ransomware-for-automated-database-extortion

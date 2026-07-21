# IOCs: Patriot Bait – AI-Assisted C&C Botnet (Russian-Speaking Actor "bandcampro")

**Source:** https://thehackernews.com/2026/07/russian-speaking-hacker-uses-google.html
**Date collected:** 2026-07-20

ip_address:
- 213.165.51.115
- 34.34.57.141
- 34.34.81.129

domain:
- tralalarkefe.com
- payloads.tralalarkefe.com
- antipublic.net

url:
- https://payloads.tralalarkefe.com/agent_final.ps1

## Additional Indicators from Trend Micro

The following are supplementary IOCs from the Trend Micro analysis (do not fit standard IOC types but are critical for detection):

**File Path:**
- %APPDATA%\Microsoft\Windows\Runtime\svchost.exe
- %TEMP%\win_update_svc_*.ps1

**Registry:**
- HKCU:\...\Run\WindowsUpdateManager
- HKCU:\Environment\UserInitMprLogonScript

**WMI:**
- Filter: Win32_SystemHealth
- Consumer: Win32_HealthConsumer

**Scheduled Tasks:**
- Microsoft\Windows\WindowsUpdate\Automatic App Update
- OneDrive Standalone Update Task-S-1-5-21-*

**HTTP Header:**
- X-Agent-ID: HOSTNAME_USERNAME

**API Endpoints:**
- GET /api/v1/update
- POST /api/v1/telemetry
- GET /api/v1/agents
- POST /api/v1/interact

## MITRE ATT&CK / ATLAS Mapping

| Tactic | ID | Technique |
|---|---|---|
| Execution | T1059.001 | PowerShell |
| Persistence | T1546.003 | WMI Event Subscription |
| Persistence | T1053.005 | Scheduled Task/Job |
| Persistence | T1547.001 | Registry Run Keys |
| Defense Evasion | T1036.005 | Masquerading: Match Legitimate Name |
| Defense Evasion | T1132.001 | Data Encoding: Standard Encoding |
| Defense Evasion | T1572 | Protocol Tunneling |
| Command and Control | T1071.001 | Web Protocols |
| Command and Control | T1102 | Web Service |
| ML/AI | AML.T0054 | LLM Jailbreak |

## Pages visited

- L1: https://thehackernews.com/2026/07/russian-speaking-hacker-uses-google.html
- L2: https://www.trendmicro.com/en_us/research/26/g/actor-behind-patriot-bait-used-ai-to-deploy-c2-botnet.html
- L3: https://documents.trendmicro.com/assets/txt/Patriot-Bait-Used-AI-for-C2-Botnet-IoC-tElIRKr.txt

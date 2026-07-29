# IOCs: GoGRPC Backdoor / Fake IT Calls via Microsoft Teams

**Source:** https://hackread.com/fake-it-calls-microsoft-teams-gogrpc-backdoor/
**Date collected:** 2026-07-28

## Summary

This campaign involves threat actors posing as IT helpdesk staff via Microsoft Teams (vishing), convincing victims to approve Quick Assist sessions. Once accessed, attackers deploy the GoGRPC backdoor (variants: Lep, Giver, Pet, Kind) and supporting tools (BlindDoor, RevSocket, PyGRPC, RSOX, S3Siphon). The threat actor is likely an initial access broker for ransomware operations.

Original research by Zscaler ThreatLabz (published July 27, 2026). The IOC section at the bottom of the Zscaler blog post (containing IP addresses, hashes, and additional domains) was truncated due to heavy website navigation boilerplate and could not be fully extracted. No GoGRPC-specific IOCs have been published to the ThreatLabz/iocs GitHub repo yet.

domain:
- re102.fastwinnow.com

url:
- https://re102.fastwinnow.com/download/link

## Pages visited

- L1: https://hackread.com/fake-it-calls-microsoft-teams-gogrpc-backdoor/ (no IOCs - news summary article)
- L2: https://www.zscaler.com/blogs/security-research/helpdesk-hijackers-teams-vishing-quick-assist-and-gogrpc-backdoor (IOC section truncated - extracted 1 domain, 1 URL from visible text)
- L2: https://www.microsoft.com/en-us/security/blog/2026/04/18/crosstenant-helpdesk-impersonation-data-exfiltration-human-operated-intrusion-playbook/ (no IOCs - general playbook)

## Notes

- The PowerShell download command from the Zscaler blog shows: `$u="hXXps:\/\/re102.fastwinnow[.]com/download/link"`
- The blog states that GoGRPC "Base64 decodes one or more hardcoded IP addresses" for C2 communication, but these IPs were in the truncated section.
- The gRPC C2 servers listen on port 443 with endpoint `/agent.AgentService/Connect` (or `/Refuse/Connect` for Kind variant)
- Additional IOCs (C2 IPs, file hashes, additional domains) were listed in the truncated IOC section of the original Zscaler blog at: https://www.zscaler.com/blogs/security-research/helpdesk-hijackers-teams-vishing-quick-assist-and-gogrpc-backdoor

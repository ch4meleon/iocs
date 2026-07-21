# IOCs: HollowGraph Malware & Cavern Framework (Cavern Manticore)

**Source:** SecurityWeek, Group-IB, Check Point Research
**Date collected:** 2026-07-21

## Summary

HollowGraph is a malware component that abuses the Microsoft 365 (Graph API) calendar as a dead-drop C&C channel. It is linked to the Cavern framework used by the Iran-nexus threat actor Cavern Manticore (MOIS-linked, overlaps with Lyceum/OilRig). IOCs were harvested from three sources: SecurityWeek news article (L1), Group-IB technical blog (L2), and Check Point Research Cavern Manticore analysis (L3).

---

## Indicators

### domain

- auth.hospitalinstallation.com
- cloudlanecdn.com
- google.com.hospitalinstallation.com

### sha1

- f1b2d650c5b7e4c598e808c727e867b71d27f4b3

---

## Additional contextual indicators (not structured into standard IOC types)

These include file paths, filenames, mutex names, and distinctive strings useful for detection:

**File paths:**
- C:\ProgramData\WinDir\WinDirStat.exe
- C:\ProgramData\WinDir\uxtheme.dll

**Filenames (malware components):**
- logAzure.txt (HollowGraph config)
- config.txt (Cavern agent config, JSON format)
- id.txt (Cavern agent, older build — plain 7-char ID)
- uxtheme.dll (Cavern Agent — trojanized DLL, Mixed-Mode C++/CLI)
- n-HTCommp.dll (Cavern communication module — NativeAOT)
- mhm.dll (Cavern file manager module)
- db.dll (Cavern SQL browser module)
- ode.dll (Cavern LDAP module)
- n-ten.dll (Cavern network recon module)
- n-sws.dll (Cavern tunnel/SOCKS5 module)

**Mutex names:**
- MYMUTEX123HELLP
- MYMUTEX123HELLP02
- MYMUTEX123HELLP04

**Distinctive error strings:**
- "What is this sh*t?! where is get_version?!?"
- "DLL not found...Maybe you didn't upload it!!!"

## Pages visited

- L1: https://www.securityweek.com/new-hollowgraph-malware-abuses-microsoft-365-calendar-for-cc-communication/ (no IOCs — news summary)
- L2: https://www.group-ib.com/blog/hollowgraph-microsoft-365/ (domain: cloudlanecdn.com, filename: logAzure.txt, sha1 from URL)
- L3: https://research.checkpoint.com/2026/cavern-manticore-exposing-iran-linked-modular-c2-framework/ (domains, file paths, filenames, mutexes, strings)

# IOCs: Hackers Strike Minnesota Water Utilities / Iran-Linked Water Sector Targeting

**Source:** https://securityaffairs.com/196246/hacking/hackers-strike-minnesota-water-utilities-one-plant-briefly-offline.html
**Date collected:** 2026-07-29

## Summary

These articles describe cyberattacks against US water utilities (Minnesota, July 2026) and related Iranian-linked targeting of water/energy control systems. The investigations are ongoing, and **no specific technical IOCs (IP addresses, domain names, file hashes, or attacker URLs) were published** in any of the three articles crawled. The articles describe tactics, techniques, and procedures (TTPs) at a narrative level without disclosing the specific indicators.

email:
- pierluigi.paganini@securityaffairs.co
  *(Note: This is the author's contact email appearing in the site footer/boilerplate. Not a threat-related IOC.)*

## Additional context (non-IOC indicators of compromise)

The following items were mentioned in the articles but do not fit the defined IOC type format. They are noted here for situational awareness:

**Threat actor names:**
- Handala (pro-Iran hacktivist group, linked to Void Manticore)
- Iranian-affiliated APT group (unnamed per CISA advisory AA26-097A)

**Malware names (not hashes):**
- win.handala (wiper)
- Handala Wiper
- Hamsa Wiper

**Observed OT ports targeted (TTPs):**
- 22 (SSH)
- 102 (Siemens industrial protocol)
- 502 (Modbus)
- 2222 (EtherNet/IP)
- 44818 (Rockwell Automation)
- 10000 (RTKBase HTTP management)

**Vendor tools abused by attackers:**
- Studio 5000 (Rockwell Automation)
- EcoStruxure Control Expert (Schneider Electric)
- TIA Portal (Siemens)

**Related CISA advisory:** https://www.cisa.gov/news-events/cybersecurity-advisories/aa26-097a

## Pages visited

- L1: https://securityaffairs.com/196246/hacking/hackers-strike-minnesota-water-utilities-one-plant-briefly-offline.html (no IOCs)
- L2: https://securityaffairs.com/195991/apt/iran-linked-actors-breach-are-targeting-us-water-and-energy-control-systems.html (no IOCs)
- L3: https://securityaffairs.com/193565/uncategorized/iran-linked-handala-breached-a-california-water-utility-it-could-have-done-worse-and-it-knows-that.html (no IOCs)

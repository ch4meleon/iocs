# IOCs: CISA warns of hackers exploiting Langflow, N-central, Apache Tomcat flaws

**Source:** https://www.bleepingcomputer.com/news/security/cisa-warns-of-hackers-exploiting-langflow-n-central-apache-tomcat-flaws/
**Date collected:** 2026-08-06

Note: No malicious IP addresses, file hashes, or confirmed-bad domains are
published in the article set. The values below are the advisory, vendor, and
research endpoints referenced by the articles (CISA KEV / alerts, NVD, N-able
status, KEVIntel, Unit 42, Horizon3, Sysdig, GuidePoint). The actual attack
indicators mentioned but NOT listed inline are: 4 source IPs on N-able's
hotfix page (status.n-able.com, see URL below), 64 source IPs in KEVIntel
CVE-2026-0770 sensor telemetry (kevintel.com, see URL below), and the Unit 42
reverse-shell campaign report. N-able also lists two host-level IOCs in the
same advisory: a registered service named 'Cloudflared' and 'svchost.exe'
present in the user's Documents folder.

domain:
- blog.kevintel.com
- beta.shodan.io
- cisa.gov
- github.com
- guidepointsecurity.com
- horizon3.ai
- kevintel.com
- nvd.nist.gov
- status.n-able.com
- sysdig.com
- try.cloudflare.com
- unit42.paloaltonetworks.com
- uptime.n-able.com
- zerodayinitiative.com

url:
- https://blog.kevintel.com/cve-2026-0770-exploited-in-the-wild-langflow-rce-added-to-cisa-kev/
- https://beta.shodan.io/search?query=html%3An-central
- https://beta.shodan.io/search?query=http.html_hash%3A944222210
- https://github.com/cloudflare/cloudflared/releases
- https://github.com/langflow-ai/langflow/pull/6911
- https://github.com/langflow-ai/langflow/releases/tag/1.3.0
- https://github.com/langflow-ai/langflow/releases/tag/1.4.0
- https://horizon3.ai/attack-research/disclosures/unsafe-at-any-speed-abusing-python-exec-for-unauth-rce-in-langflow-ai/
- https://kevintel.com/CVE-2026-0770#sensor-telemetry
- https://nvd.nist.gov/vuln/detail/cve-2026-34486
- https://nvd.nist.gov/vuln/detail/CVE-2026-0770
- https://nvd.nist.gov/vuln/detail/CVE-2026-18556
- https://nvd.nist.gov/vuln/detail/CVE-2026-18577
- https://status.n-able.com/2026/08/02/n-central-2026-3-hotfix-1-mitigation-for-cve-2026-18577/
- https://status.n-able.com/2025/08/13/announcing-the-ga-of-n-central-2025-3-1/
- https://try.cloudflare.com/
- https://unit42.paloaltonetworks.com/autonomous-ai-cyber-attack-campaign/
- http://uptime.n-able.com/event/201454/
- http://uptime.n-able.com/event/201456/
- https://www.cisa.gov/known-exploited-vulnerabilities-catalog?field_cve=CVE-2026-0770
- https://www.cisa.gov/known-exploited-vulnerabilities-catalog?search_api_fulltext=CVE-2025-8875&field_date_added_wrapper=all&field_cve=&sort_by=field_date_added&items_per_page=20&url=
- https://www.cisa.gov/known-exploited-vulnerabilities-catalog?search_api_fulltext=CVE-2025-8876&field_date_added_wrapper=all&field_cve=&sort_by=field_date_added&items_per_page=20&url=
- https://www.cisa.gov/news-events/alerts/2026/08/04/cisa-adds-three-known-exploited-vulnerabilities-catalog
- https://www.cisa.gov/news-events/alerts/2026/07/21/cisa-adds-four-known-exploited-vulnerabilities-catalog
- http://www.cisa.gov/news-events/alerts/2025/05/05/cisa-adds-one-known-exploited-vulnerability-catalog
- https://www.cisa.gov/news-events/alerts/2025/08/13/cisa-adds-two-known-exploited-vulnerabilities-catalog
- https://www.guidepointsecurity.com/blog/tunnel-vision-cloudflared-abused-in-the-wild/
- https://www.sysdig.com/blog/jadepuffer-agentic-ransomware-for-automated-database-extortion
- https://www.zerodayinitiative.com/advisories/ZDI-26-036/

## Pages visited

- L1: https://www.bleepingcomputer.com/news/security/cisa-warns-of-hackers-exploiting-langflow-n-central-apache-tomcat-flaws/ (no IP/hash/domain IOCs)
- L2: https://www.bleepingcomputer.com/news/security/cisa-orders-feds-to-patch-actively-exploited-langflow-rce-flaw/
- L2: https://www.bleepingcomputer.com/news/security/n-able-warns-of-n-central-auth-bypass-flaw-exploited-in-attacks/
- L2: https://www.bleepingcomputer.com/news/security/critical-langflow-rce-flaw-exploited-to-hack-ai-app-servers/
- L3: https://www.bleepingcomputer.com/news/security/cisa-warns-of-n-able-n-central-flaws-exploited-in-zero-day-attacks/ (no IOCs)
- L3: https://www.bleepingcomputer.com/news/security/jadepuffer-ransomware-used-ai-agent-to-automate-entire-attack/ (no IOCs)
- L3: https://www.bleepingcomputer.com/news/security/hackers-increasingly-abuse-cloudflare-tunnel-for-stealthy-connections/ (no IOCs)

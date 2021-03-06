AVPWN
=====

List of real-world threats against endpoint protection software - For future reference. The list is based on public information and thus is obviously incomplete. 

The list should include:
  * Non-public 0-day exploits at the time of reference
  * Public incidents where attackers exploited endpoint protection software 
  * Supporting public evidence should be provided for all records

The list doesn't include: 
  * Exploits intentionally disclosed to the vendor in any way (including full uncoordinated disclosure)
  * Detection bypasses, because I don't want to fill up the storage space of GitHub
  * Attacks or exploits against perimeter products, because I'm lazy

The List
--------

| Name                                                                        | Link                                                   | Internal ID | Server Side | Client Side | Known Incident |
|-----------------------------------------------------------------------------|--------------------------------------------------------|-------------|-------------|-------------|----------------|
| avast! Local Information Disclosure                                         | https://wikileaks.org/hackingteam/emails/emailid/45441 | 13-005      |           0 |           1 |       Brokered |
| avast! Local Privilege Escalation                                           | https://wikileaks.org/hackingteam/emails/emailid/45441 | 13-010      |           0 |           1 |       Brokered |
| McAfee ePolicy Orchestrator Privileged Remote Code Execution                | https://wikileaks.org/hackingteam/emails/emailid/45441 | 13-019      |           1 |           0 |       Brokered |
| McAfee ePolicy Orchestrator Post-Auth Privileged Remote Code Execution      | https://wikileaks.org/hackingteam/emails/emailid/45441 | 13-023      |           1 |           0 |       Brokered |
| McAfee ePolicy Orchestrator Post-Auth Privileged Remote Code Execution      | https://wikileaks.org/hackingteam/emails/emailid/45441 | 13-024      |           1 |           0 |       Brokered |
| ESET NOD32 Antivirus and ESET Smart Security Remote Pre-auth Code Execution | https://wikileaks.org/hackingteam/emails/emailid/45441 | 2010-0021   |           0 |           1 | Brokered, Sold |
| Symantec AntiVirus Remote Stack Buffer Overflow  | http://www.securityfocus.com/news/11426 | CVE-2006-2630   |           0 |           1 | Exploited ItW |
| McAfee Stinger Portable DLL Sideloading  | https://wikileaks.org/ciav7p1/cms/page_27492400.html | Fine Dining  |           0 |           1 | CIA collection |
| Sophos Virus Removal Tool DLL sideloading | https://wikileaks.org/ciav7p1/cms/page_27263043.html | Fine Dining  |           0 |           1 | CIA collection |
| Kaspersky TDSS Killer Portable DLL Sideloading | https://wikileaks.org/ciav7p1/cms/page_27492393.html | Fine Dining  |           0 |           1 | CIA collection |
| ClamWin Portable DLL Hijack | https://wikileaks.org/ciav7p1/cms/page_27262995.html | Fine Dining  |           0 |           1 | CIA collection |
| Kaspersky ?? SUID command injection | https://hackmd.io/s/r1gLMUUpx | evolvingstrategy  |           0 |           1 | EQGRP exploit leaked by Shadow Brokers  |
| Symantec rastlsc.exe DLL side-loading | https://www.welivesecurity.com/wp-content/uploads/2018/03/ESET_OceanLotus.pdf| OceanLotus | 0 | 1 | ESET report |
| Trend Micro Office Scan server ZIP path traversal | https://www.zdnet.com/article/trend-micro-antivirus-zero-day-used-in-mitsubishi-electric-hack/ | CVE-2019-18187 | 1 | 0 | Mitsubishi Electric |
| Trend Micro Apex One and OfficeScan migration tool RCE | https://www.darkreading.com/vulnerabilities---threats/trend-micro-patches-two-zero-days-under-attack/d/d-id/1337338 https://success.trendmicro.com/solution/000245571 https://www.tenable.com/blog/cve-2020-8467-cve-2020-8468-vulnerabilities-in-trend-micro-apex-one-and-officescan-exploited-in | CVE-2020-8467 | 1 | 0 | N/A |
| Trend Micro Apex One and OfficeScan content validation escape | https://www.darkreading.com/vulnerabilities---threats/trend-micro-patches-two-zero-days-under-attack/d/d-id/1337338 https://success.trendmicro.com/solution/000245571 https://www.tenable.com/blog/cve-2020-8467-cve-2020-8468-vulnerabilities-in-trend-micro-apex-one-and-officescan-exploited-in | CVE-2020-8468 | 0 | 1 | N/A |

### Immortal exploits

The following list contains exploits of ["immortal" vulnerabilities](https://www.rand.org/pubs/research_reports/RR1751.html) - ones that for some reason can't be fixed by the vendor.

| Name                                                                        | Link                                                   | Internal ID | Server Side | Client Side | Known Incident |
|-----------------------------------------------------------------------------|--------------------------------------------------------|-------------|-------------|-------------|----------------|
| Avast aswSnx.sys Kernel Driver 11.1.2253 - Memory Corruption Privilege Escalation | https://artemonsecurity.blogspot.com/2016/10/remsec-driver-analysis-agnitum-driver.html https://twitter.com/cherepanov74/status/762654147841781760 | N/A | 0 | 1 | Remsec / Cremes malware |
| Agnitum Sandbox.sys Kernel Driver Arbitrary DLL Loading | https://artemonsecurity.blogspot.com/2016/10/remsec-driver-analysis-agnitum-driver.html https://twitter.com/cherepanov74/status/762654147841781760 | N/A | 0 | 1 | Remsec / Cremes malware |

### Honorable mentions

* As of November 2016. Zerodium (a prominent vulnerability broker) [is offering](https://web.archive.org/web/20161108134847/http://zerodium.com/program.html) up to $40.000 for Antivirus LPE/RCE
  * In 2017. the price for AV LPE exploits [dropped](https://web.archive.org/web/20170823152044/https://zerodium.com/program.html) to $10.000 (presumably because of the easy accessibility to such exploits). 
* In 2014. Kaspersky [reported](https://web.archive.org/web/*/https://kasperskycontenthub.com/wp-content/uploads/sites/43/vlpdfs/unveilingthemask_v1.0.pdf) that the Careto malware was attempting to exploit a vulnerability in their products _"to make the malware 'invisible' in the system"_. The targeted vulnerability was fixed in 2008.
* In 2015. Kaspersky [reported](https://blog.kaspersky.co.uk/kaspersky-statement-duqu-attack/5858/) a compromise of their own systems. According to the report _"neither [Kaspersky's] products nor services have been compromised"_, and attackers were after information about _"ongoing investigations [...] detection methods and analysis capabilities"_. In 2017 [NYT reported](https://www.nytimes.com/2017/10/10/technology/kaspersky-lab-israel-russia-hacking.html) that Kaspersky was compromised by the Israeli intelligence that found that Russian services were using the companies infrastructure/products to "scour the world for U.S. secrets".
* In 2013. Bit9, a security firm mostly known for it's white-list based endpoint protection product, [was hacked](https://krebsonsecurity.com/2013/02/security-firm-bit9-hacked-used-to-spread-malware/) and code-signing certificates with private keys were stolen. With these, attackers were able to sign malware with Bit9's code-signing certificate. The signed malware was used to bypass Bit9 protection on the client.   
* In May 2019. Advanced Inteligence LLC [claimed](https://www.advanced-intel.com/blog/top-tier-russian-hacking-collective-claims-breaches-of-three-major-anti-virus-companies) that Fxmsp - a threat actor they've been monitoring for some time - compromised four antivirus companies including [Symantec, Trend Micro, and McAfee](https://www.reddit.com/r/netsec/comments/bok8kx/fxmsp_claims_breaches_of_three_major_antivirus/). Fxmsp was said to sell access to the source code and internal networks on the darknet. Advanced Intelligence LLC [was registered](https://twitter.com/swagitda_/status/1126548346624270337) right before the announcement in Delaware.
  * In May 2019, Based on Symantec's [statement](https://www.cbronline.com/news/trend-micro-symantec-fxmsp), Advanced Intelligence retracted from their claim that Symantec was affected. Trend Micro acknowledged the breach of "a single testing lab network".
  * In June 2019,  Advanced Intelligence [claimed](https://www.bleepingcomputer.com/news/security/another-hacker-selling-access-to-charity-antivirus-firm-networks/) further breaches, including Comodo.

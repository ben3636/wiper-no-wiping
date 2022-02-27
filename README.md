# Wiper No Wiping!
Public Repo for the collection and documentation of IOC's and detections for the novel data-wiping malware used in Ukraine

![alt text](https://github.com/ben3636/wiper-no-wiping/blob/main/image.jpg)

## TLDR // Sparknotes - What Should I Do Right Now?
* **Patch all the things!**
   * Apply vendor security updates on endpoints, servers, etc asap

* **Leverage Vulnerability Scanners**
   * Identify vulnerable machines and prioritize patching/updating in order of asset criticality
   * Defending against zero-day exploits is more complicated but we do know that this malware has been previously deployed leveraging known exploits
   * Don't be low-hanging fruit :)

* **Update AV Software & IDS Rules**
   * There is a good chance your vendors have already released updates to help defend against this threat
   * Clicking an update button is one of the easiest wins (someone else has already done the work)

* **Backup Now**
   * If you haven't backed up critical data in a bit, now's a good time
   * Offline backups are your friend, otherwise ensure backup servers are well-protected (see above)



## Specific Vulnerabilities That Have Been Leveraged - Patch These NOW!
* Apache Tomcat
* Microsoft Exchange
* Microsoft SQL Priv-Esc (CVE-2021-1636)



## How Can We Detect/Prevent The Malware?
* **Use Defense in Depth**
   * Use detection methods at different layers
      * Endpoint & Network 
* **Educate users on phishing and social engineering threats!**
   * You are the best AV
   * Users are always a target, and they're always harder to patch

* **Deploy black-and-white signatures**
   * File hashes (endpoint and network)
      * I've compiled a list of hash values for this malware here: https://github.com/ben3636/wiper-no-wiping/blob/main/hash-brown.md
   * Known DNS queries & IP Addresses
      * These may be used for C2 or component download, either way you should keep an eye on them: https://github.com/ben3636/wiper-no-wiping/blob/main/dns-ip.md

* **Deploy behavioral detections**
   * We may not know which technique the attacker will use, but we can watch for specific behaviors linked to high-level goals
   * Wouldn't it be cool if someone made this into a detailed/easy-to-read framework? You're in luck :)
      * https://attack.mitre.org



## Items in This Repo
* **Hash List (hash-brown.md)**
   * This is a combined list of hashes for known-nasty files related to the malware
   * This list can be used to create IDS & EDR rules in bulk for easy detection

* **Domain & IP List (dns-ip.md)**
   * This is a combined list of domains and servers I've seen mentioned in relationt to this malware
   * I would be flagging (and/or blocking) these items to identify items that may be infected
   * These servers may be used for C2 or component download
      * If it's the second item, it may be possible to stop it from downloading additional components needed to detonate (here's hoping)

## Central Document (Migrating Entirely to this Repo Soon)
https://docs.google.com/document/d/1KK2hCH9WmwACVup7VTIAYEgVzGcZsaqUlx0J_IFtmt0/edit?usp=sharing


## Coming Soon
* Suricata rules
* Elastic XDR rules



## Reading Material

https://www.cisa.gov/uscert/shields-technical-guidance

https://www.cisa.gov/uscert/ncas/alerts/aa22-057a

https://symantec-enterprise-blogs.security.com/blogs/threat-intelligence/ukraine-wiper-malware-russia

https://www.cyberark.com/resources/blog/hermeticwiper-what-we-know-about-new-malware-targeting-ukrainian-infrastructure-thus-far

http://blog.talosintelligence.com/2022/02/threat-advisory-hermeticwiper.html

https://www.zscaler.com/blogs/security-research/hermetic-wiper-resurgence-targeted-attacks-ukraine

https://zetter.substack.com/p/second-wiper-attack-strikes-systems?utm_source=url

https://www.ired.team/offensive-security/credential-access-and-credential-dumping/dump-credentials-from-lsass-process-without-mimikatz

https://www.sentinelone.com/labs/hermetic-wiper-ukraine-under-attack/

https://www.microsoft.com/security/blog/2022/01/15/destructive-malware-targeting-ukrainian-organizations/

https://securityintelligence.com/posts/new-destructive-malware-cyber-attacks-ukraine/

https://www.crowdstrike.com/blog/how-crowdstrike-falcon-protects-against-wiper-malware-used-in-ukraine-attacks/

https://socradar.io/what-you-need-to-know-about-russian-cyber-escalation-in-ukraine/



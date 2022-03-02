## See Below for Domains, IP's, & Network Behavior Known to be Related to this Malware
> I highly recommend at least alerting on these servers in firewall/netflow and DNS logs. Blocking certain ones may be even better as it could prevent the malware from completing its build process (preventing final detonation)

* trustsecpro[.]com

* whatismyip[.]com

* confluence[.]novus[.]ua

## Source: https://www.zscaler.com/blogs/security-research/hermeticwiper-resurgence-targeted-attacks-ukraine

* coagula[.]online
* deer.dentist.coagula[.]online
* declaration.deed.coagula[.]online
* surname192.temp.swtest[.]ru
* 94.158.244[.]27
* kfctm[.]online
* my.cloud-file[.]online
* my.mondeychamp[.]xyz
* files-download.infousa[.]xyz
* download.logins[.]online

### URL's

* http://surname192[.]temp.swtest[.]ru/prapor/su/ino.gif
* http://surname192[.]temp.swtest[.]ru/prapor/su/derg.gif
* http://surname192[.]temp.swtest[.]ru/prapor/su/flagua.gif
* http://surname192[.]temp.swtest[.]ru/prapor/su/flages.gif
* 94.158.244[.]27/absolute.ace
* 94.158.244[.]27/distant.cdr
* http://kfctm[.]online/0802adqeczoL7.msi
* http://my.cloud-file[.]online/Microsoft_VieweR_2012.msi
* http://my.mondeychamp[.]xyz/uUi1rV.msi
* http://my.mondeychamp[.]xyz/ReadMe.msi
* http://files-download[.]infousa[.]xyz/Windows_photo_viewers.msi
* http://files-download[.]infousa[.]xyz/Windows_photo_viewer.msi
* http://download.logins[.]online/exe/LinK13112020.msi


## Source: https://www.welivesecurity.com/2022/03/01/isaacwiper-hermeticwizard-wiper-worm-targeting-ukraine/

> Note: As described in this article, the worm component of this malware will scan the /24 subnet to enumerate hosts and scan a few common ports to determine live neighbors:

### WMI Spreader (Dest Ports Scanned)

* 20: ftp

* 21: ftp

* 22: ssh

* 80: http

* 135: rpc

* 137: netbios

* 139: smb

* 443: https

* 445: smb


> While we do know that the order of the ports is randomized to prevent fingerprinting, I'm looking into statistical detection opportunities grounded in the the burst of low-packet activity involving this group of ports within a given time window

### SMB Spreader (SMB Pipes)

* samr

* browser

* netlogon

* lsarpc

* ntsvcs

* svcctl

### SMB Spreader Hard-Coded Credentials

* Usernames

   * guest

   * test

   * admin

   * user

   * root

   * administrator

   * manager

   * operator

* Passwords

   * 123

   * Qaz123

   * Qwerty123


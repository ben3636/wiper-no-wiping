# Process Arguments & Commandline String IOCs

## Source: https://www.welivesecurity.com/2022/03/01/isaacwiper-hermeticwizard-wiper-worm-targeting-ukraine/

* regsvr32.exe /s /i <path>
 
* regsvr32.exe /s /i:-s <path>
 
* rundll32 <current folder>\<6 random letters>.ocx #1 -s <path to HermeticWizard> – i <target IP>
  
* C:\windows\system32\cmd.exe /c start C:\windows\system32\\regsvr32.exe /s /i C:\windows\<filename>.dll
 
* cmd /c start regsvr32 /s /i ..\\<filename>  & start cmd /c \”ping localhost -n 7 & wevtutil cl System\”

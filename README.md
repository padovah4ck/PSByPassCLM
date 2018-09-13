# PSByPassCLM
Bypass for PowerShell Constrained Language Mode

# Description
This technique might come in handy wherever or whenever you're stuck in a low privilege PowerShell console
and PowerShell Version 2 engine is not available to perform a [PowerShell Downgrade Attacks](http://www.leeholmes.com/blog/2017/03/17/detecting-and-preventing-powershell-downgrade-attacks/)

What described above may happen in [modern] Windows OSes, like Windows 10, that nowdays are shipped out with AppLocker
and PowerShell Version 5 (v5).

AppLocker in Allow mode and PowerShell running in Constrained Mode, it is not possible for an attacker 
to change the PowerShell language mode to full in order to run attack tools

"PowerShell v5 detects when AppLocker Allow mode is in effect and sets the PowerShell language to Constrained Mode, severely limiting the attack surface on the system.
With AppLocker in Allow mode and PowerShell running in Constrained Mode, it is not possible for an attacker to change the PowerShell language mode to full in order to run attack tools." [[Source]](https://adsecurity.org/?p=2604)
 

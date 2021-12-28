# powershell - Get WM objects

Format: 
	
```powershell
Get-WmiObject -Class "<class-name>" -Property "<prop-name>"
```

Example:

```powershell
Get-WmiObject -Class "Win32_Processor" | Format-List
```

[More Info](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1)

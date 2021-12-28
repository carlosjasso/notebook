# PowerShell - create shortcut

Examples:

```powershell
#$fso = new-object -ComObject scripting.filesystemobject
#$fso.CreateFolder("$env:ProgramData + \Microsoft\Windows\Start Menu\Programs\TTLNK")

$Shell = New-Object -ComObject ("WScript.Shell")
$ShortCut = $Shell.CreateShortcut($env:ProgramData + "\Microsoft\Windows\Start Menu\Programs\Volume.lnk")
$ShortCut.TargetPath="c:\Windows\System32\sndvol.exe"
#$ShortCut.Arguments="-arguementsifrequired"
$ShortCut.WorkingDirectory = "c:\Windows\System32";
$ShortCut.WindowStyle = 1;
#$ShortCut.Hotkey = "CTRL+SHIFT+F";
$ShortCut.IconLocation = "c:\Windows\System32\sndvol.exe, 0";
$ShortCut.Description = "Volume";
$ShortCut.Save()

$Shell = New-Object -ComObject ("WScript.Shell")
$ShortCut = $Shell.CreateShortcut($env:ProgramData + "\Microsoft\Windows\Start Menu\Programs\Date & Time.lnk")
$ShortCut.TargetPath="C:\Windows\system32\rundll32.exe"
$ShortCut.Arguments="shell32.dll,Control_RunDLL timedate.cpl,,0"
$ShortCut.WorkingDirectory = "C:\Windows\System32";
$ShortCut.WindowStyle = 1;
#$ShortCut.Hotkey = "CTRL+SHIFT+F";
$ShortCut.IconLocation = "%SystemRoot%\System32\SHELL32.dll, 20";
$ShortCut.Description = "Date & Time";
$ShortCut.Save()

$Shell = New-Object -ComObject ("WScript.Shell")
$ShortCut = $Shell.CreateShortcut($env:ProgramData + "\Microsoft\Windows\Start Menu\Programs\Teams.lnk")
$ShortCut.TargetPath="%LocalAppData%\Microsoft\Teams\Update.exe"
$ShortCut.Arguments='--processStart "Teams.exe"'
$ShortCut.WorkingDirectory = "%LocalAppData%\Microsoft\Teams\";
$ShortCut.WindowStyle = 1;
#$ShortCut.Hotkey = "CTRL+SHIFT+F";
$ShortCut.IconLocation = "%LocalAppData%\Microsoft\Teams\app.ico, 0";
$ShortCut.Description = "Microsoft Teams";
$ShortCut.Save()
```

# powershell - Allow an app in the windows firewall

Allow Example:

```powershell
New-NetFirewallRule -DisplayName "<display-name>" -Direction Inbound -Program "<path/to/.exe>" -RemoteAddress LocalSubnet -Action Allow
```

Block Example:

```powershell
New-NetFirewallRule -DisplayName "Chrome Update" -Direction Inbound -Program "C:\Program Files (x86)\Google\Update\GoogleUpdate.exe" -Action Block
```

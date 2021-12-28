# Powershell - Get drive encryption status

_Note:_ This command has to be run in an elevated profile.

```powershell
Get-WmiObject -Namespace root\CIMV2\Security\MicrosoftVolumeEncryption -Class Win32_EncryptableVolume
```

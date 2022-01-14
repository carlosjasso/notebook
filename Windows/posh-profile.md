# Powershell Profile

Powershell (posh) reads it's equivalent to bash profile (~/.bashrc) from its `$PROFILE` env var.

```powershell
echo $PROFILE
```

> *Outoput:* `C:\Users\<user>\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1`

Within this file, one can set aliases, environment variables and prompt configuration.

Example:

```powershell
# Custom Prompt setup
function prompt {
  $dir = Get-Location
  if ($dir.tostring() -eq $HOME) {
    $dir = "~"
  } else {
    $dir = Split-Path -leaf -path (Get-Location)
  }
  Write-Host ($env:USERNAME) -NoNewline -ForegroundColor Green
  Write-Host ("@" + $env:COMPUTERNAME +":") -NoNewline
  Write-Host $dir -NoNewline -ForegroundColor Green
  Write-Host ">" -NoNewline
  ' ' # ! This is important
  # Similar style but colorless
  # '{0}@{1}:{2}> ' -f $env:USERNAME, $env:COMPUTERNAME, $dir
}

# variables and aliases
$CODE = "C:\code"
Set-Alias -Name py -Value "C:\Program Files\Python310\python.exe"
```

# Powershell - WMI searcher

Example:

```powershell
$objSearch = [WMISEARCHER]"SELECT * FROM WmiMonitorBasicDisplayParams"
$objSearch.Scope = "\\.\ROOT\WMI"
$objSearch.Get()
```

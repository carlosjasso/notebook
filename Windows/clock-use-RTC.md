# USE RTC on Windows

Create and run a `.reg` file with the following

```reg
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINESYSTEMCurrentControlSetControlTimeZoneInformation]
     RealTimeIsUniversal=dword00000001
```

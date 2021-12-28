# Windows DOS - Add local admin

Local:

```bat
net localgroup administrators <username>@<domain> /add
```

Azure:

```bat
net localgroup administrators AzureAD\<username>@<domain> /add
```

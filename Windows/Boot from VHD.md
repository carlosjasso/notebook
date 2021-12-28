# Windows - Boot from VHD

- Add VHD to Windows Boot Configuration Data:  
`bcdboot <Drive Letter>:\windows`  
Example: `bcdboot F:\windows`  
- Check current BCD configutation: `bcdedit`
- Modify BCD entry Description:  
`bcdedit /set {<flag>} Description “Enter desired description”`  
Example:  
`bcdedit /set {default} Description “Windows Server 2012”`
- Set default entry: `bcdedit /default <ID>`
- Delete entry from BCD: `bcdedit /delete {UUID}`

_Do not forget to detach VHD and change default BCD entry after process_

- Rebuild BCD (recovery mode with CMD):  
`bootrec /rebuildbcd`

**Advanced**

- Create BCD in external device  
`bcdboot <path_to_windows_in_vhd> /s <drive_with_external_BCD> /f ALL`  
example:  
`bcdboot T:\Windows /s D: /f ALL`

`bcdedit /store <path_to_store> ...`

example: `bcdedit /store D:\boot\bcd`

**extras**

`bcdedit /timeout <number_of_seconds>`
`bcdedit /set {bootmgr} displaybootmenu yes`

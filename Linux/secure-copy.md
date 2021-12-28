# scp - Secure Copy

to push a file

`scp <sourcefile> <username>@<hostname>:[destinationpath/filename]`

`scp <file_path>.md5 <hostname>:`  
_^ will assume user is "current" user, and destination file will assume "same as source"_

to 'pull' a file, you put the hostname in the source

`scp <hostname>:*.md5 .`

You can run the command from server 'a' and copy a file from server 'b' to server 'c'
`scp <username>@<hostname-b>:/var/log/file.txt <username>@<hostname-c>:blah.txt`

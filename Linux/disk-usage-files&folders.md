# Disk usage of files and folders

For files:

```bash
find <dir-path> -type f -size +100000 -exec du -sh {} \;
```

for directories:

```bash
find /home -maxdepth 1 -type d -exec du -sh {} \;
```

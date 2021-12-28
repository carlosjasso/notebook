# Compare directories content

`cd` into the source directorty and:

```bash
find . -type f -exec md5sum {} \; >> /<path>/<filename>.md5
```

`cd` into compared directory and:

```bash
md5sum -c --quiet /<path>/<filename>.md5
```

_note:_ `grep` can be used to filter undesired patterns. Example:

```bash
grep -v -e "<x>" -e "/<x>/"
```

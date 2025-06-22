```
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
```


stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

human-readable in a file: `strings`

preceded by several ‘=’ characters : `grep "="` (several characters "==")

# strings filename | grep "=="



```
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

Helpful Reading Material
Piping and Redirection
```

the only line of text that occurs only once. It mean only one non-repeating containt pasword

At this level I will use 

- sort  : sort lines in alphabetical order default is ascending
- uniq -u  :  print only lines that appear exactly one. 
- and pipe to filter out unique line

## cat filename | sort | uniq -u

must be in order `sort` and next is `uniq -u`. if reverse it, the lines are duplicated and not adjacent → uniq will not detect

![image](https://github.com/user-attachments/assets/02c35384-3623-4880-8838-c88af973aff5)


---
# Note

`uniq` (including uniq -u) only work on consecutive duplicate lines


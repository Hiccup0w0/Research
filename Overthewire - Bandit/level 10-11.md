```
The password for the next level is stored in the file data.txt, which contains base64 encoded data

Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

Helpful Reading Material
Base64 on Wikipedia
```

They give us a based 64 encoded data string

the decription says the string is base64 but you can check with cyberchef -> magic mode or sometimes you can rely on "==" at the end of string

we can solve it by `base64 -d filename`  -d is decode  

or echo "encoded string" | base64 -d

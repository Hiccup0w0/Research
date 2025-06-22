```
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

Helpful Reading Material
Rot13 on Wikipedia
```

![image](https://github.com/user-attachments/assets/ecbebb3a-4667-4cb8-9087-1c6ddc0119b9)


int data.txt file will have a string  `Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4`  it is rot13 cuz the decription says

and ROT13 encoding will replace a letter with another letter 13 positions away from it. EX "Hello" with ROT13 encoding is `H -> U` `e -> r` `l -> y` `l -> y` `o -> b`. Uryyb

So to solve  Iit just used ROT13 encoding for this string cuz it will rotate the 13th letter back to the correct position.

## cat file name | tr 'A-Za-z' 'N-ZA-Mn-za-m'

tr 'set1' 'set2'

set1 is a original string like abCd and set2 is the way how it will decode or encode by move the letter position 13times. `tr` command will replace each character from set 1 with charecters rotated 13 times.


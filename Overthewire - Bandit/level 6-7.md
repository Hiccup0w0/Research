```
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size
Commands you may need to solve this level
ls , cd , cat , file , du , find , grep
```

use `ls` you will see doesn't has any file or direc at here

it owned by user bandit 7 and group bandit6. I try use `find -type f -user bandit7 -group bandit6 -size 33c` but it doesn't work cuz this command will only find at current directory

Cuz this command only searches the current directory and subdirectories within it, not entire system. The decription hint is `stored somewhere on the server`

`find / -type f -user bandit7 -group bandit6 -size 33c`

by add `/` to comamnd it will search the entire system, starting at the root directory (/). And if there are too many special directories taht are denied permission , you can use `2>/dev/null` at the end of the command

2> will redirect errors and `/dev/null` will hide errors

![image](https://github.com/user-attachments/assets/5d2f4f8d-516c-4969-8cfd-c5f32ee63c91)


---
#note

`/`  this represents the root directory

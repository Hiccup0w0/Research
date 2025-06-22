```
The password for the next level is stored in the file data.txt next to the word millionth

Commands you may need to solve this level
man, grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
```

Pretty obvious, the password is stored at data.txt and next to the word `millionth`

  so in linux you can find any word or text in a file by combining  `cat <filename>`with using `grep` . EX cat data.txt | grep "word" 

`|` : pipe (concatenate commands)

the output of previous command will be input of next command

![image](https://github.com/user-attachments/assets/7e466748-ffc1-414d-938c-b2ca02983408)




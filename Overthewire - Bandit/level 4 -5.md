```
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

Commands you may need to solve this level
ls , cd , cat , file , du , find
```
you can `cat` each file but if they have 100 files, you will very be very tired. And describe also mentions about `file`

the description hint given is `only human-readable file ` so you can use `file <file>` to check type of this file. `file ./*` to check for all files in this directory 

![image](https://github.com/user-attachments/assets/e9d03310-ddd4-49bd-a25a-05b876d4aab2)


and only ascii text , human can read it so You need to `cat ` this file   

---
# Note

`./*` : wildcard syntax mean all the files and folders in current di  rectory 

./ : is current directory

* : wildcard for any file name in a directory.


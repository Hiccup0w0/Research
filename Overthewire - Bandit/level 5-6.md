```
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable
Commands you may need to solve this level
ls , cd , cat , file , du , find
```


A file has all properties

- human-readable
- 1033 bytes in size
- not executable

`file -type f -size 1033c -not executable`
+  `-type f` is a regular file
+  `-size 1033c` is 1033 bytes
+  and it is not a executable file


![image](https://github.com/user-attachments/assets/30e80bdb-0654-45ab-9eba-7e691f98ac55)


![image](https://github.com/user-attachments/assets/53447253-2acf-4049-b943-3a51031a92f7)


---
![image](https://github.com/user-attachments/assets/5363cd66-1694-44cb-bfbd-32ba1f7db35c)

and like you see file2 has `.` before it so it is hidden file
`cat ./maybehere07/.file2`

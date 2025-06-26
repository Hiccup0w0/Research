![image](https://github.com/user-attachments/assets/f7872f43-aa46-4d93-8370-8234973088d8)


ở đây có 1 thư mục inhere và như phần mô tả thì file đã bị ẩn đi, chỉ cần dùng `ls -la` list all là có thể thấy 

```
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Apr 10 14:23 .
drwxr-xr-x 3 root    root    4096 Apr 10 14:23 ..
-rw-r----- 1 bandit4 bandit3   33 Apr 10 14:23 ...Hiding-From-You
```

Ở dòng số 3 có 1 tên file là "... Hiding-From-You" có thể vì tiền tố ...nên linux có thể nhầm nó với 1 tên file hệ thống nên không thể hiện bằng `ls`. Có thể in nội dung trong nó ra bằng cách dùng `cat "filename"` 

## bandit3@bandit:~/inhere$ cat "...Hiding-From-You" à không cần để nó trong dấu "" "__"

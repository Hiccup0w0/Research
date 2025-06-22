```
The password for the next level is stored in a hidden file in the inhere directory.

Commands you may need to solve this level
ls , cd , cat , file , du , find
```

you will see a directory `inhere` but when you go there by `cd` it you will not see anything cuz file is hidden

```
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Apr 10 14:23 .
drwxr-xr-x 3 root    root    4096 Apr 10 14:23 ..
-rw-r----- 1 bandit4 bandit3   33 Apr 10 14:23 ...Hiding-From-You
bandit3@bandit:~/inhere$ find
.
./...Hiding-From-You
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
```

`ls -la `(list -list all), it will show all file and directory even hidden things

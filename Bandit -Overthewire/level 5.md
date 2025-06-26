![image](https://github.com/user-attachments/assets/a5233fd2-164e-486b-b6b7-af6ada8b586c)

![image](https://github.com/user-attachments/assets/a9752779-baf1-4882-8f43-2a016a9d8cd0)


như phần mô tả thì file chứa pass nằm trong đống đường thư mục này và thỏa mãn các điều kiện:

- human-readable
- 1033 bytes in size
- not executable

  với file human-readable ta có thể loại `-type f` là 1 file bình thường
  1033 bytes thì là `-size 1033c`
  và đó là 1 file không thể thực thi thì là `! -executable`

 ![image](https://github.com/user-attachments/assets/d02ccf18-c449-4933-a9d6-e283475d4e47)

![image](https://github.com/user-attachments/assets/454b500f-1ede-4c43-b30b-0edd057d1190)

và `find` trong linuz giúp tìm file theo điều kiện của file đó 
```
bandit5@bandit:~/inhere$ find -type f -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ find -type f -size 1033c -not -executable
./maybehere07/.file2
```

---
# Note

`-executable ` là 1 biểu thức kiểm tra chứ ko phải 1 option.
  

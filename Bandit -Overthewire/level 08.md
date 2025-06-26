![image](https://github.com/user-attachments/assets/d30bbb07-db74-47a7-9824-f4dff8e09da0)


ở bài này ta sẽ tìm 1 chuỗi duy nhất, độc nhất không trung với bất kì chuỗi nào, mình có tìm đại 1 chuỗi

```
bandit8@bandit:~$ cat data.txt |grep "nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE"
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
nOu0uI9qll3ws9FtaQt7mE4ngAmMAsfE
```

ở đây mình sẽ dùng `cat, sort, uniq -u` và dùng pipe để kết hợp bọn chúng lại với nhau

`Pipe` | : aka ống nối, nó có thể lấy output của câu lệnh trước biến thành input của câu lệnh sau.

`sort` có thể sắp xếp các dóng theo thứ tự của bẳng chữ cái dòng 1 aaa, dòng 2 bbbb,...

`uniq`  in ra 1 dòng xuất hiện đúng 1 lần,  lưu ý là uniq dù là với bất cứ option thêm vào nào thì cx chỉ loại bỏ dòng trùng nhau nếu chúng nằm liền kề. VD:

```
aaa
bbb
ccc
ccc
aaa
```

thì khi chạy uniq thì nó sẽ chỉ loại bỏ thằng ccc ở dòng só 4 vì chúng nằm kế nhau và thằng aaa thì không. Chính vì vậy cần dùng lệnh `sort` trước `uniq -u` để đảm bảo chạy đúng ra đoạn cần

![image](https://github.com/user-attachments/assets/0ea4aa70-57d7-4ae4-b7f8-c0e2f7ce238e)


## cat filename | sort | uniq -u


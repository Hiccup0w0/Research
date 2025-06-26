![image](https://github.com/user-attachments/assets/def940d1-0cc8-4fd8-b154-bef0d4498850)


Ở level này sẽ có 1 file khá đặc biệt đó là `-` file aka dash-named file. File này chỉ là 1 dấu `-` và không thể in nội dung trong file ra chỉ bằng lệnh `cat`

Phải dùng thêm `cat ./-` 

Với việc thêm `./` linux sẽ hiểu đó là 1 file thật sựchứ không phải 1 option hay 1 cái gì khác, `./` nghĩa là thư mục hiện tại và linux sẽ hiểu `-` là 1 file trong thư mục hiện tại. 


![image](https://github.com/user-attachments/assets/165e4533-a33a-41e8-8150-d4f281c69087)


mô tả level này cũng giống level trước nhưng hãy chú ý đến `somewhere on server` 

cx như level trc với câu lệnh `find -type f -user bandit7 -group bandit6 -size 33c` nhưng nó lại không hiện bất cứ thứ gì.

Vì lệnh `find` chỉ tìm các file trong thư mục hiện tại và thư mục con trong đó thôi , và như phần nói ở trên đâu đó trong server nghĩa là file ta cần tìm không nằm trong thư mục hiện tại và tư mục con trong đó.

Nên mình sẽ thêm `/` vào lệnh `find / -type f -user bandit7 -group bandit6 -size 33c`. Với việc thêm `/` nó sẽ tìm kiếm trong toàn hệ thống server bắt đầu từ thư mục root,  Và nếu có quá nhiềù thư mục mà bạn bị chặn không cho truy cập "Permission denied"

thì nên thêm `2>/dev/null`  vào cuối câu lệnh thì nó sẽ ẩn nhưng cái thư mục bạn không thể truy cập vào

![image](https://github.com/user-attachments/assets/17265aed-2509-4388-aedd-569864eb2885)


---
# Note

`/` là biểu diễn thư mục gốc

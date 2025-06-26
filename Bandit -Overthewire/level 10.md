
![image](https://github.com/user-attachments/assets/ed06ddfa-9120-453a-99f8-aa100b79bbd3)


![image](https://github.com/user-attachments/assets/78419501-8ee3-4846-8610-35b439244f40)


cho nhưng ai không đọc đề bài thì đây là 1 chuỗi được mã hóa dữ liệu bằng base64, có thể thỉnh thoảng nhận diện bằng ký tự "==" ở cuối nhưng nó cũng chỉ là tương đối thôi vì có nhiều cách để làm nó trở nên khó nhận biết hơn như là mã hóa nó với 1 lớp mã hóa khác

Và còn 1 cách nữa là vừa để xem nó là chuỗi gì vừa để giải mã là vào `cyberchef.io` chọn chế đọ magic mode dùng khi bạn không biết đấy là chuỗi gì và nó sẽ tự đọng giải mã nó  

Giải mã bằng command : `echo "chuỗi bị mã hóa base64" | base64 -d` -d là decode 

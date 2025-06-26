![image](https://github.com/user-attachments/assets/c35e9b85-735d-44f4-82d6-4514db69cfa8)


có thể nhận mk cho level tiếp bằng cách gửi mk level hiện tại đến port 30001 on locahost bằng mã hóa SSL/TSL 

### SSL/TSL
>
> SSL/TLS là giao thức mã hóa dữ liệu truyền tải giữa client và server

và muốn kết nối có mã hóa SSL/TSL thì dùng openssl s_client để tạo ra 1 kết nối an toàn đến port 30001

## openssl s_client -connect localhost:30001

với `openssl` command nó đang gọi công cụ mã hóa OpenSSL giúp hỗ trợ mã hóa, giải mã và giao tiếp ssl, `s_client` là để giả lập 1 client và kết nối đến cổng cần cần tới trên bằng `-connect localhost:30001`
 
 hoặc

 ## ncat --ssl localhost 30001

 về chức năng thì cơ bản ncat --ssl cũng giống openssl s_client đều có mã hóa SSL/TLS, nhưng 1 số cong dụng khác còn kém.

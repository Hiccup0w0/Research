![image](https://github.com/user-attachments/assets/42c54e91-bb04-4162-bf02-5c47260972d3)

` submitting the password of the current level to a port on localhost in the range 31000 to 32000` , these ports have a server listening on them, find out which of those speak SSL/TLS and  wgichs don't, 1 server that will give the next credentials 

mình sẽ quét các cổng từ cổng 31000-32  và xem cổng nào sử dụng dịch vụ SSL/TLS phản hồi lại thì sẽ đến cổng đấy 

## nmap -sV localhost -p 31000-32000

Dùng nmap là công cụ để quét các địa chỉ và cổng trong 1 server. Nó sẽ gửi thông điệp (packets) đến từng cổng trong khoảng 31-32 và sẽ chờ xem cổng nào phản hồi lại, đây là 1 công cụ mã nguồn mở. Nó sẽ rất hữu ích về sau [Nmap](https://www.freecodecamp.org/news/what-is-nmap-and-how-to-use-it-a-tutorial-for-the-greatest-scanning-tool-of-all-time/)

vì đề bài mô tả là xem cổng nào dùng dịch vụ TLS/SSL nên sẽ dùng thêm option `-sV` service và Version, vì nó sẽ cố xác đinh dịch vị và phiên bản của mỗi cổng nên sẽ quét rất lâu.

Hoặc cũng có thể quét chay trước bằng `nmap localhost -p 31000-32000` để xem cổng nào mở rồi mới xem dịch vụ chúng đang dùng `nmap -sV localhost -p 31046,31518,31691` không nhanh hơn tí nào

![image](https://github.com/user-attachments/assets/98c39175-5c92-48fd-948b-994b6c9192fe)

sau khi chạy xong lệnh thì bạn sẽ thấy cái bẳng này là các cổng mở đã phản hồi lại thông điệp, với kết nối TCP và dịch vụ SSL, ở đây có 2 cổng dùng dịch vụ SSL đó 1 cái service là echo và 1 cái không biết, vậy mình cũng loại luôn cổng có echo vì nó chỉ pin những gì mình nhập

 
## openssl s_client -connect localhost:31790 -quiet

với lệnh openssl thì sẽ kết mối đến 1 server thông qua dục vụ SSL/TLS và xem thông tin của dịch vụ đó

và option `-quiet` sử dụng để ẩn đi KeyUPdate: 1 kĩ thuật đổi khóa mã hóa giữa client và server. VD bạn đang có 1 mật khẩu cho két và bên trong két là mật khẩu khóa nhàthì KEYUPDATE sẽ đổi mật khẩu khóa két của bạn và sẽ không tác đọng gì đến mật khẩu bên trong, `nó ngăn cản bạn mở két thôi` 

![image](https://github.com/user-attachments/assets/5165587b-9127-43f6-88b2-ed668bc1038b)

và khi đã có đuược RSA private key thì sẽ tạo 1 file chứa nó và cấp quyền đọc viết cho owner `600` xong kết nối đến bandit 17  và vì không có quyền viết nội dung vào file ở thư mục home nên hãy dùng cách tạo thư mục mới ở /tmp

##  ssh -i privatekey bandit17@localhost -p 2220 

privatekey là file mình tạo để chứa private key 

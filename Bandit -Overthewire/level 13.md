![image](https://github.com/user-attachments/assets/5546ca0b-23d2-4ada-b075-328563f633da)


mật khẩu để vào bandit14 là ở trong `/etc/bandit_pass/bandit14` only be read by user bandit14, a private SSH key that can be used to login, localhost is a hostname refers to the machine you are working on.

Ở level này ta sẽ dùng private key để đến level 14 và lấy mật khẩu cho level 14 ở đó. `Private key` là 1 phương thức dùng để  xác thực khi không dùng mật khẩu để đang nhập vào máy chủ.

mình thấy 1 file `sshkey.private` 

![image](https://github.com/user-attachments/assets/f52580c6-bc35-4828-bfc8-d3de13b01aa3)

đây là định dạn PEM cho RSA Private Key, nó dùng để xác thực cho SSH (giao thúc bảo mật) bằng public key. ta sẽ dùng nó để đang nhập vào bandit14 

Mình đọc trong cái helpful matarial thì lấy priavte key như sau 

## ssh -i sshkey.private bandit14@localhost -p 2220

trong đó `ssh` là để kết nối đến máy chủ,  `-i privatekeyname` là để xác nhận dùng private key từ file có khóa RSA , `badit14@lbandit.labs.overthewire.org ` laf host name mà máy tính của mình đang làm việc với ở đây là bandit14 server và port mạc định của overthewire

Ở đây có vẻ là file chứa khóa RSA private key đã đucợ cấp quyền rồi, còn thường thì phải cáp quyền cho nó `chmod 600 privatekeyname` cấp quyền đọc và viết cho chủ sở hữu

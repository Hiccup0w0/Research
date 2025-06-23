```
Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

Commands you may need to solve this level
ssh, telnet, nc, openssl, s_client, nmap

Helpful Reading Material
SSH/OpenSSH/Keys
```

Private key là phương thức được dùng để xác thực khi không dùng mật khẩu để đăng nhập vào máy chủ. Ta sẽ sử dụng file này để "ssh" vào bandit14

![image](https://github.com/user-attachments/assets/194e3926-9ac6-4007-94bb-d2710a8059fd)

## ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

Lưu lại file sshkey.private vào máy

Khi tạo file, Linux sẽ cho quyền mặc định

Cho nên phải đổi quyền của file chỉ dành cho chủ sở hữu nếu không sẽ báo lỗi


The authenticity of host '[bandit.labs.overthewire.org]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).



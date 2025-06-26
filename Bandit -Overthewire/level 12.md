![image](https://github.com/user-attachments/assets/727bd734-e804-43b9-af95-29dea537aa7e)

bài mệt nhất :((

```
bandit12@bandit:~$ cat data.txt
00000000: 1f8b 0808 41d4 f767 0203 6461 7461 322e  ....A..g..data2.
00000010: 6269 6e00 0149 02b6 fd42 5a68 3931 4159  bin..I...BZh91AY
00000020: 2653 59a8 ffa7 8f00 001d 7fff dbeb 7ffa  &SY.............
00000030: bb7f a5ef bb7e f5fb fdff b7c7 f3ff ff7f  .....~..........
00000040: ff7f fff7 deba fdfa eff7 dddf b001 3b19  ..............;.
00000050: a200 d01a 0190 0034 0006 800d 0340 0346  .......4.....@.F
00000060: 8000 0340 0320 0069 a034 0640 0346 4680  ...@. .i.4.@.FF.
00000070: 68d1 a68c 8321 9313 4da4 f510 6406 8003  h....!..M...d...
00000080: 4006 9a00 000d 000d 0069 a007 a9a0 001a  @........i......
00000090: 1b50 03d4 01a6 9a1e a001 a343 4683 469a  .P.........CF.F.
000000a0: 3d40 001a 7a8d 01a0 074c 801e a1a6 8064  =@..z....L.....d
000000b0: 01a3 d434 00c4 0d00 000d 0001 a680 1a19  ...4............
000000c0: 0061 0f53 41a0 0000 0d00 341a 0320 0034  .a.SA.....4.. .4
000000d0: d1ea 0168 4882 8244 0130 5550 f16b f52e  ...hH..D.0UP.k..
000000e0: a322 cb9f bb8c aaf6 e244 cc70 b151 47c8  .".......D.p.QG.
000000f0: 6c03 a3ae 4a81 1ee0 03ce 840e a978 2046  l...J........x F
00000100: 630b 4b0d 9883 7078 e7e8 5bfb 68f1 f685  c.K...px..[.h...
00000110: 6f46 771c 3920 449f f0cb 39e2 0841 10b5  oFw.9 D...9..A..
00000120: 8714 e981 115c d1bc 2da4 318b 106c 904e  .....\..-.1..l.N
00000130: 9328 5e97 405a 4054 21db e049 1a32 5f3d  .(^.@Z@T!..I.2_=
00000140: 7069 408f f0a4 8ce5 fbea 282c 51d1 49e4  pi@.......(,Q.I.
00000150: d52f 0762 dd90 27b8 79d3 0499 52e0 060c  ./.b..'.y...R...
00000160: fd91 a474 d408 88f3 1fda d2d1 325a baeb  ...t........2Z..
00000170: bfe7 f0f6 cc3c 776d f369 e73c 47d4 66ea  .....<wm.i.<G.f.
00000180: 4b90 e404 03b3 6a09 4687 945d 09ef 706b  K.....j.F..]..pk
00000190: 8f82 2503 80d0 0a0a 3e60 f879 bf02 2d42  ..%.....>`.y..-B
000001a0: bf37 9c96 4b22 585c 35c8 3cf1 da9f 518b  .7..K"X\5.<...Q.
000001b0: ccd5 a68c 9647 aa38 8a50 89d2 f89c 1ff0  .....G.8.P......
000001c0: 1042 18c3 6549 400d fe17 ec74 3171 6d74  .B..eI@....t1qmt
000001d0: a8bb 0def f11a 5a69 0e70 aa34 0037 b180  ......Zi.p.4.7..
000001e0: 1540 c4d2 0af7 e290 8784 ce9e 147a 6836  .@...........zh6
000001f0: 944b 3f18 2ba2 c620 af92 fb01 184f 3def  .K?.+.. .....O=.
00000200: 1b7d 0162 733d adca 90ac 7142 8319 f703  .}.bs=....qB....
00000210: 5930 69e2 8320 9110 5d63 0db9 9294 d4ef  Y0i.. ..]c......
00000220: 50b9 5907 0924 92c1 014e a284 25ce a6ef  P.Y..$...N..%...
00000230: 67b2 4e06 6d21 4136 2ac0 292d 6638 033c  g.N.m!A6*.)-f8.<
00000240: 21af be4e 13bb b74f 2c10 18c7 eea3 c436  !..N...O,......6
00000250: c988 05e6 5638 1ff1 7724 5385 090a 8ffa  ....V8..w$S.....
00000260: 78f0 d951 192d 4902 0000                 x..Q.-I...
```

đống sữ liệu trên là 1 dữu liệu hex trong 1 hexdump file nhưng nhìn vào đóng dữ liệu hex trên ở đoạn đầu là `1f8b` là magic number của .gunzip 1 kĩ thuật nén file và 1 đoạn ở đoạn dầu bên bảng text `data2.bin` 

thì đây có thể là 1 file nhị phân bị chuyển đổi dữ liệu bằng công cụ `xxd` đó là 1 công cụ dùng chuyển đổi dữ liệu giũa dữ liệu nhị phân và dữ liệu hiển thị bằng text (hex)

vậy nên mình đã chuyển dịch người lại bằng `xxd -r data.txt > data` chuyển đống dữ liệu hex từ data.txt sang data file

và thêm 1 vẫn đề nữa là không thể tạo 1 file mới ở thư mục hiện home tại được `create a directory under /tmp in which you can work`

```
bandit12@bandit:~$ xxd -r data.txt > data
-bash: data: Permission denied
```
vậy nên mình đã tạo 1 thư mục trong thư mục /tmp `mkdir /tmp/hiii` 

# Note

`/tmp` là 1 thư mục tạm thời trong hệ điều hành linux , nó chứa các file tru tạm thời do người dùng tạo ra, ở đó user sẽ có quyền để tạo ra thư mục tạm thời của họ, và tránh ảnh hưởng đến người chơi khác, nên là đặt quả tên nào ít đụng hàng thôi. 

và dữ liệu bạn tạo ra cũng sẽ bị xóa nếu restart hệ thống

sau khi tạo xong thư mục thì mình  copy nó vào thư mục của mình  `cp data.txt /tmp/hiii` về thu mục home bằng cd ~ . xong rồi thì chuyển lại dữ liệu file thôi

![image](https://github.com/user-attachments/assets/0e43c5bd-5954-4ef0-bffc-a53f2b0f0b54)

đến dây sẽ bắt đầu quá trình giải nén, có 3 phương thức nén chính ở bài này là nén bằng công cụ gunzip, bunzip2 và tar. và mỗi khi giải nén xong sẽ ra 1 file khác bị nén nữa, mình gọi là nén nhiều lớp. Và mỗi lần giải nén xong 1 file 

cần dúng `file` để kiểm tra xem nó là loại file bị nến theo kiểu gì. Như cái trên là bị nén bởi `gunzip` chỉ cần quan tâm câu đầu thôi còn mấy câu sau là thông tin file trước khi bị nén thôi

để giải nén cần lặp lại các bước:

```
mv filename filename.gz
gzip -d filename.gz  hoặc gunzip filename.gz
```
vì gzip là công cụ dùng để nén file nên phải thêm option -d (decompress) vào không thì nó sẽ báo lỗi là dẫ bị nén rồi 

![image](https://github.com/user-attachments/assets/daff6d7e-98e5-4cd8-b840-566b3bcee5cd)

bắt đầu 1 vòng mới, dùng `ls, file` để check, sau khi giải nén file data.gz thì sẽ mất đi file cũ thay vào đó là file bị giải nén và ở đây là1 file nén bằng `bzip2`, cách giải cũng gần như giống gunzip

![image](https://github.com/user-attachments/assets/00c80e79-31bb-454b-a805-f1a7f55647fd)

và cuối cùng là tar file

![image](https://github.com/user-attachments/assets/b16dfd7d-43e1-408e-8253-534fba8ee5ff)

đoạn đầu tương tự, đoạn sau giair nén khác, dùng `tar -xvf filename.tar` 
- -x là extract
- -v là verbose thực ra cái này không nhất thiết có, lợi ích nó sẽ liệt kê những file nào đã giải nén ra vì khi giải nén file tar nó có thể mở ra nhiều tệp tin và file tar đó không bị xóa nên dễ nhầm lần xíu
- -f là file đucợ chỉ định

tiếp tục đến khi nó ra 


```
data8: ASCII text
```








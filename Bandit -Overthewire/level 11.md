![image](https://github.com/user-attachments/assets/e1d21db2-23fe-469c-87bd-91a5949c3ef6)

thêm 1 kiểu mã hóa dữ liệu nữa , đây là ROT13

![image](https://github.com/user-attachments/assets/4e0ba85a-2c80-4de4-a93e-33b452a1d58e)

nó khá đơn giản thôi, trong bẳng chữ cái tiếng anh có 26 chữ cái A-Z , và mã hóa ROT13 là việc di chuyểnchữ cái được chỉ định đến vị trí thứ 13 trên bảng chữ cái đó

xếp 26 chữ cái theo 2 hàng ngang,  13 chữ cái dầu tiên ở hàng đầu đứng đầu là A và 13 chữ cái còn lại ở hàng 2 đứng đầu là N, thì khi A bị dính ROT13 thì nó sẽ biến thành N và tương tự.

Chính vì vậy cách giải mã 1 chuỗi bị dính ROT13 cũng chính là mã hóa chính nó

`Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4`

# echo "encoded string" | tr 'A-Za-z' 'N-ZA-Mn-za-m'

đoạn sau là đoạn mã hóa/ giải mã ROT13 translate set1 là  như 1 chuỗi bình thường "hello" và set 2 là chuỗi encode/decode ROT13 sẽ biến hello --> Uryyb và ngược lại . với set2 mn có thể dựa vào cái ảnh về ROT13 mình lấy trong wiki để viết


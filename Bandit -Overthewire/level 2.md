![image](https://github.com/user-attachments/assets/6964d6d6-b72d-46c7-890b-b69da21fbc81)


Ở level này bạn sẽ nhận được 1 file dặc biệt như là `aaa bbb ccc` đó là 1 file nhưng có khoẳng trắng ở giữa. Linux sẽ không thể mở file này vì nó sẽ nghĩ đây là 3 file khác biệt

vì cậy cần có dấu `\` backslash key hay trong TH này nó gọi là `escaping` linux sẽ hiểu \ là khoẳng trắng trong file . VD `cat aaa\bbb\ccc`. 

hay 1 cách khác là quoting `""` tất cả những gì trong "" được linux coi là 1 tham số . VD `cat"aaa bbb ccc"`

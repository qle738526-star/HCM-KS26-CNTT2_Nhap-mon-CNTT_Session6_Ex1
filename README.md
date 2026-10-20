# HCM-KS26-CNTT2_Nhap-mon-CNTT_Session6_Ex1

## Phần 1: Phân Tích Lỗi Sai

* **Lỗi 1 (Sai cú pháp tạo và di chuyển thư mục chứa khoảng trắng):**
  * **Nguyên nhân:** Nam dùng lệnh `mkdir Smart Farm Project` và `cd Smart Farm Project` nhưng không bọc tên thư mục trong dấu ngoặc kép (`""`). Trong PowerShell, khoảng trắng được hiểu là dấu phân cách giữa các tham số độc lập. 
  * **Hậu quả:** Hệ thống hiểu lầm Nam đang tạo hoặc di chuyển giữa nhiều tham số rời rạc (`Smart`, `Farm`, `Project`) thay vì một thư mục thống nhất, dẫn đến lỗi cú pháp hoặc không tìm thấy đường dẫn.

* **Lỗi 2 (Sai quy ước ký tự phân cách đường dẫn trong PowerShell):**
  * **Nguyên nhân:** Nam sử dụng dấu xược xuôi `/` trong lệnh `mkdir src/sensors/temperature`. 
  * **Hậu quả:** Mặc dù PowerShell trên các phiên bản hiện đại có thể châm chước hiểu được, nhưng chuẩn thống kê và an toàn nhất trên hệ điều hành Windows PowerShell là sử dụng dấu xược ngược `\` (`src\sensors\temperature`).

## Phần 2: Hoàn Thiện (Chuỗi Lệnh Tối Ưu)

Để hoàn thành toàn bộ cấu trúc thư mục lồng nhau một cách chính xác và ít dòng lệnh nhất, Nam chỉ cần sử dụng **1 dòng lệnh PowerShell** duy nhất sau:

mkdir "Smart Farm Project\src\sensors\temperature"

# Giải thích:

* Sử dụng dấu ngoặc kép "" để bảo vệ chuỗi đường dẫn có chứa khoảng trắng.

* Lệnh mkdir trong PowerShell có khả năng tự động tạo đệ quy toàn bộ chuỗi thư mục lồng nhau  chỉ trong một thao tác duy nhất mà không cần phải dùng lệnh cd để di chuyển vào trong.

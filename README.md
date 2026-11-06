# Bài 5: Chuẩn hóa quy trình hỗ trợ kỹ thuật nội bộ

## 1. Thiết kế sơ đồ luồng (Flowchart)

Khi gặp lỗi cài đặt môi trường, thành viên cần thực hiện theo quy trình sau:

```
BẮT ĐẦU
   |
   v
Gặp lỗi kỹ thuật
   |
   v
Ghi lại thông báo lỗi và chụp ảnh
   |
   v
Tra cứu Google (site:stackoverflow.com)
   |
   v
Tìm được giải pháp phù hợp?
   |
   +---- CÓ ----------------------+
   |                             |
   |                             v
   |                  Kiểm tra độ tin cậy
   |                  và tính an toàn
   |                             |
   +---- KHÔNG                    |
         |                       |
         v                       |
   Hỏi AI Assistant              |
         |                       |
         v                       |
   Yêu cầu AI giải thích         |
   và hướng dẫn sửa lỗi          |
         |                       |
         +-----------------------+
                     |
                     v
             Giải pháp an toàn?
                     |
          +----------+----------+
          |                     |
         CÓ                  KHÔNG
          |                     |
          v                     v
    Thử sửa lỗi          Không thực hiện,
    và kiểm tra lại      tìm nguồn khác
          |                     |
          v                     |
    Đã sửa được lỗi?            |
          |                     |
     +----+----+                |
     |         |                |
    CÓ       KHÔNG              |
     |         |                |
     v         v                |
 Viết Bug   Gửi Bug Report      |
 Report     cho nhóm hỗ trợ     |
     |         |                |
     +----+----+                |
          |                     |
          v                     |
   Lưu lại cách xử lý           |
          |                     |
          v                     |
       KẾT THÚC                 |
                                |
        (Nếu không an toàn ------+
         thì tìm nguồn khác)
```

## 2. Mẫu kịch bản gỡ lỗi thần tốc

Bước 1: Ghi nhận lỗi

- Ghi lại tên phần mềm và hệ điều hành.
- Sao chép nguyên văn thông báo lỗi.
- Chụp ảnh màn hình lỗi.

Bước 2: Tìm kiếm bằng Google

Ví dụ: Máy tính gặp lỗi `git is not recognized` khi sử dụng PowerShell.

Sử dụng câu lệnh:

```
site:stackoverflow.com "git is not recognized" PowerShell Windows -crack
```

Mục đích:

- `site:`: Tìm trong StackOverflow.
- `"..."`: Tìm chính xác thông báo lỗi.
- `-crack`: Loại bỏ kết quả chứa từ khóa crack.

Bước 3: Hỏi AI Assistant

Sử dụng Prompt mẫu:

Em là sinh viên năm nhất ngành Công nghệ thông tin, đang sử dụng Windows và PowerShell.

Khi nhập lệnh Git, em gặp thông báo lỗi:

`git is not recognized`

Hãy giúp em:

1. Dịch và giải thích lỗi bằng tiếng Việt.
2. Xác định nguyên nhân có thể gây ra lỗi.
3. Hướng dẫn cách sửa từng bước.
4. Cung cấp các lệnh cần nhập và giải thích tác dụng.
5. Cảnh báo nếu có lệnh nào có thể gây ảnh hưởng đến máy tính.

Yêu cầu: Hướng dẫn đơn giản, dễ hiểu, phù hợp với người mới học.

Bước 4: Kiểm tra và sửa lỗi

- Đối chiếu hướng dẫn từ Google và AI.
- Kiểm tra độ tin cậy của nguồn.
- Chỉ thực hiện các lệnh khi đã hiểu tác dụng và kiểm tra độ an toàn.
- Kiểm tra lại xem lỗi đã được khắc phục chưa.

Bước 5: Lập Bug Report

Ghi lại các thông tin:

- Tên lỗi: Git is not recognized.
- Nguyên nhân: Máy tính chưa cài Git hoặc chưa cấu hình PATH.
- Cách sửa: Cài Git hoặc kiểm tra lại biến môi trường PATH.
- Kết quả: Ghi rõ đã sửa thành công hay chưa.

## 3. Kết luận

Theo em, việc chuẩn hóa quy trình hỗ trợ kỹ thuật giúp các thành viên chủ động tìm hiểu và sửa lỗi trước khi nhờ người khác. Kết hợp Google, AI và Bug Report giúp tiết kiệm thời gian, hạn chế lỗi lặp lại và nâng cao hiệu quả làm việc nhóm.

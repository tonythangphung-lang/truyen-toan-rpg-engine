🟩 Task 05 — EXERCISE ENGINE (Máy sinh & xử lý bài tập toán)
🎯 Mục tiêu

Xây dựng hệ thống xử lý bài tập toán cho Story RPG:

Sinh bài tập

Nhận đáp án người chơi

Chấm điểm

Trả kết quả về Core Engine

Gắn với từng node trong story

🧱 Chức năng chính
✔ 1. Load bài tập từ Story JSON

Trong mỗi node có thể có trường:
"exercise": {
  "type": "subtraction",
  "level": 2,
  "random": true
}
Engine cần:

Đọc loại bài tập

Sinh nội dung câu hỏi

Trả dữ liệu cho UI

✔ 2. Sinh bài tập tự động

Hỗ trợ:

Phép cộng

Phép trừ

Phép nhân

Phép chia

Dạng nâng cao (để Task08 xử lý thêm)

Sinh số theo level:

level 1 → số nhỏ (0–20)

level 2 → 2 chữ số

level 3 → 3 chữ số

✔ 3. Nhận đáp án + chấm điểm

So sánh đáp án

Trả điểm: đúng → 1, sai → 0

Gửi kết quả về Core Engine (Task01)

✔ 4. Tương tác với UI

Exercise Engine không hiển thị giao diện, chỉ trả:
{
  "question": "12 - 7 = ?",
  "options": [4,5,6],
  "correctIndex": 1
}
✔ 5. Báo cáo kết quả

Trả về UI kết quả đúng / sai

Trả về Core Engine để lưu tiến trình + tăng level

📦 Output

File:
taskcards/Task05_Exercise_Engine.md

Nội dung file phải có:

Mục tiêu

Yêu cầu tính năng

Cách kết nối với Core Engine

Định dạng dữ liệu Input/Output

API dự kiến

Ví dụ JSON

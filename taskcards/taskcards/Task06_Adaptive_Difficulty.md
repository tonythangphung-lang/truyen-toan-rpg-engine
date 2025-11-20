🟦 Task 06 — ADAPTIVE DIFFICULTY (Tự động điều chỉnh độ khó)
🎯 Mục tiêu

Xây hệ thống tự động thay đổi độ khó bài tập dựa trên:

Điểm số gần đây

Tỉ lệ đúng sai

Thời gian làm bài

Level hiện tại của người chơi

Giúp game luôn vừa sức, không quá khó, không quá dễ.

🧱 Chức năng chính
✔ 1. Thu thập dữ liệu người chơi

Hệ thống cần ghi lại:

Số câu đúng liên tiếp

Số câu sai liên tiếp

Thời gian hoàn thành mỗi bài

Level hiện tại

Lịch sử 10 bài gần nhất

✔ 2. Tính toán độ khó mới

Quy tắc đề xuất:

Đúng 3 câu liên tiếp → tăng level +1

Sai 2 câu liên tiếp → giảm level -1

Thời gian quá nhanh (< 2s) → tăng nhẹ

Thời gian quá lâu (> 15s) → giảm nhẹ

Level tối thiểu: 1
Level tối đa: 10

✔ 3. Trả level mới cho Exercise Engine

Adaptive System không tạo bài tập, chỉ trả:
{
  "newLevel": 3,
  "reason": "3 correct streak"
}
✔ 4. Lưu dữ liệu vào Core Engine

Core Engine (Task01) sẽ:

Lưu lại vào tiến trình

Gửi cho Exercise Engine để sinh câu hỏi

📦 Output

File:
taskcards/Task06_Adaptive_Difficulty.md

Nội dung file bao gồm:

Mục tiêu

Chức năng

Bộ dữ liệu cần thu thập

Công thức tính độ khó

API dự kiến

Ví dụ JSON Input/Output

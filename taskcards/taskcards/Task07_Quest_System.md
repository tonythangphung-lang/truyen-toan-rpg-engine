🟦 Task 07 — QUEST SYSTEM (Hệ thống nhiệm vụ + phần thưởng)
🎯 Mục tiêu

Tạo hệ thống nhiệm vụ trong game RPG Toán:

Giao nhiệm vụ

Theo dõi tiến độ

Trả thưởng khi hoàn thành

Liên kết với tiến trình học

🧱 Chức năng chính
✔ 1. Khai báo nhiệm vụ trong story

Quest có thể nằm trong story.json:
"quests": [
  {
    "id": "q1",
    "title": "Hoàn thành 5 bài trừ",
    "targetType": "subtraction",
    "targetCount": 5,
    "reward": {
      "coins": 10,
      "exp": 20
    }
  }
]
✔ 2. Theo dõi tiến độ quest

Mỗi lần người chơi làm bài tập:

Nếu đúng loại → cộng 1

Nếu đủ số lượng → complete quest

Hệ thống track:

progress

status ("active", "completed")

✔ 3. Thưởng cho người chơi

Khi hoàn thành:

exp

tiền (coins)

item (nếu có Task09)

Quest System trả về:
{
  "questId": "q1",
  "status": "completed",
  "reward": { "coins": 10, "exp": 20 }
}
✔ 4. Lưu tiến trình

Kết nối với Core Engine để:

Lưu quest đã hoàn thành

Không reset lại khi vào game lần sau

📦 Output

File:
taskcards/Task07_Quest_System.md

Nội dung cần có:

Mục tiêu

Cách khai báo quest

Luồng theo dõi tiến độ

Kết nối với Exercise Engine + Core Engine

API Input/Output

Ví dụ JSON

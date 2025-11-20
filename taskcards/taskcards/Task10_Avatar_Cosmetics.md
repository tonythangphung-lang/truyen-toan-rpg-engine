🟪 Task 10 — AVATAR & COSMETICS (Hệ thống nhân vật + trang phục)
🎯 Mục tiêu

Tạo hệ thống tùy chỉnh nhân vật giúp game hấp dẫn hơn:

Chọn avatar ban đầu

Mở khóa trang phục khi đạt thành tích

Thay đổi skin theo tiến độ học

Kết nối với các phần thưởng từ Quest, Combat, Level

🧱 Chức năng chính
✔ 1. Avatar cơ bản

Người chơi có thể chọn:

Giới tính (tùy chọn)

Giao diện cơ bản (3–6 mẫu)

Tên nhân vật

Lưu trong tiến trình:

{
  "avatar": {
    "base": "avatar_01",
    "costume": null
  }
}

✔ 2. Hệ thống trang phục (Cosmetics)

Mỗi trang phục gồm:

{
  "id": "costume_knight",
  "name": "Chiến binh Số",
  "rarity": "rare",
  "unlock": {
    "level": 5,
    "quest": "q3",
    "achievement": "win_10_battles"
  }
}


Trang phục không tăng sức mạnh (chỉ thẩm mỹ), để tránh pay-to-win.

✔ 3. Mở khóa trang phục

Unlock bằng:

Level

Hoàn thành quest

Đánh bại boss

Hoàn thành chapter

Khi mở khóa:

{
  "status": "unlocked",
  "costume": "costume_knight"
}

✔ 4. Hệ thống trang bị avatar trong UI

Người chơi có thể:

Xem bộ sưu tập

Thử trang phục

Chọn trang phục đang mặc

📦 Output file

taskcards/Task10_Avatar_Cosmetics.md

Bao gồm:

Mục tiêu

Hệ thống avatar

Hệ thống trang phục

Unlock rules

JSON mẫu

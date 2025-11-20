🟧 Task 08 — COMBAT MATH (Chiến đấu bằng phép toán)
🎯 Mục tiêu

Tạo hệ thống chiến đấu kiểu RPG nhưng dựa trên bài tập toán:

Người chơi tấn công bằng cách làm đúng bài tập

Quái phản công nếu trả lời sai

Hệ thống máu, dame, giáp

Liên kết chặt với Exercise Engine (Task05)

🧱 Chức năng chính
✔ 1. Stats của người chơi & quái

Các thông số cơ bản:

HP (máu)

ATK (sát thương)

DEF (giáp)

Crit chance (tỉ lệ chí mạng)

Level

Ví dụ JSON:

{
  "player": { "hp": 50, "atk": 10, "def": 5 },
  "enemy":  { "hp": 40, "atk": 8,  "def": 3 }
}

✔ 2. Lượt chiến đấu (Turn-based)

Luồng:

Game tạo 1 bài tập (Exercise Engine)

Người chơi trả lời

Nếu đúng → người chơi gây sát thương

Nếu sai → quái phản công

Kiểm tra HP cả hai

Lặp lại

✔ 3. Tính sát thương

Công thức đề xuất:

damage = atk - def/2
nếu trả lời quá nhanh (< 2s) → +20% damage
nếu trả lời sai → enemy attack


Chí mạng:

crit = 1.5x damage khi random() < critChance

✔ 4. Kết thúc trận đấu

Trả về:

{
  "result": "win",
  "playerHp": 18,
  "enemyHp": 0,
  "expReward": 30,
  "coinsReward": 5
}

📦 Output file

taskcards/Task08_Combat_Math.md

Gồm:

Mục tiêu

Stats

Luồng chiến đấu

Công thức damage

Kết nối Exercise Engine

JSON Input/Output

🟦 Task 02 — STORY SCHEMA (Chuẩn hóa JSON toàn hệ thống)
🎯 Mục tiêu

Xây dựng chuẩn JSON chính thức cho game truyện toán đa nhánh.
Schema này giúp:

AI khác tạo story đồng nhất

Core Engine dễ đọc – dễ parse

Không lỗi khi load map / render UI

Mở rộng dễ: nhiệm vụ, chiến đấu, item, cơ chế khác…

📦 Cấu trúc tổng thể story.json
{
  "start": "startNodeId",
  "meta": {
    "title": "Tên truyện",
    "version": "1",
    "author": "Tên tác giả hoặc AI",
    "description": "Mô tả ngắn"
  },

  "nodes": {
    "nodeId": {
      "title": "Tên của node",
      "text": "Đoạn mô tả nội dung của node",
      "media": {
        "img": "url hoặc đường dẫn ảnh",
        "audio": "url hoặc đường dẫn âm thanh"
      },
      "map": {
        "x": 50,
        "y": 70
      },

      "choices": [
        {
          "text": "Nội dung lựa chọn",
          "description": "Mô tả phụ",
          "target": "id_node_khác",

          "condition": {
            "minScore": 0,
            "requiredItem": "id_item"
          },

          "effects": {
            "score": +1,
            "giveItem": "id_item",
            "removeItem": "id_item"
          }
        }
      ],

      "exercise": {
        "type": "minus_integer",
        "level": 1,
        "data": { }
      }
    }
  }
}
🧩 Quy tắc quan trọng
1. Mỗi node phải có ID duy nhất

Ví dụ:
start
hall
choiceA
bossFight
ending
2. Mỗi choice phải có target

Nếu không → engine lỗi.

3. Hệ trục map (x, y)

x: 0–100

y: 0–100
Dùng cho Map Renderer (Task04).

4. exercise để gắn bài tập toán

Khi node có bài tập → engine gọi startExercise().

🔥 Output yêu cầu

File:
taskcards/Task02_Story_Schema.md
Chứa toàn bộ nội dung trên.

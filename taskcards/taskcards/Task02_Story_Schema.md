# Task 02 — STORY SCHEMA (Chuẩn hóa JSON cho toàn bộ hệ thống)

## Mục tiêu
Xây dựng bộ **chuẩn JSON chính thức** cho game truyện toán đa nhánh.
Schema này giúp:
- AI khác tạo story đồng nhất
- Core Engine dễ đọc và xử lý
- Không lỗi khi load map / load exercise
- Mở rộng dễ dàng (nhiệm vụ, chiến đấu, item…)

Schema này là nền móng số 1 của hệ thống.

--------------------------------------------

## Cấu trúc tổng thể của file story.json

{
  "start": "startNodeId",
  "meta": {
    "title": "Tên truyện",
    "version": 1,
    "author": "Tên tác giả hoặc AI",
    "description": "Mô tả ngắn"
  },
  "nodes": {
    "<nodeId>": {
      "title": "Tên của node",
      "text": "Đoạn mô tả nội dung",
      "media": {
        "img": "url hoặc đường dẫn",
        "audio": "url hoặc đường dẫn"
      },
      "map": {
        "x": 50,    // % vị trí (0–100)
        "y": 70
      },
      "choices": [
        {
          "text": "Tên lựa chọn hiển thị",
          "description": "Mô tả phụ",
          "target": "nodeId_khác",
          "condition": {
            "minScore": 0,   // mở khi đủ điểm
            "requiredItem": "id_vật_phẩm"


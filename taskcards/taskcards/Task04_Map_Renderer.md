Task 04 — MAP RENDERER (Hiển thị bản đồ story + liên kết giữa các node)
🎯 Mục tiêu

Xây dựng module hiển thị bản đồ story dạng graph (kiểu cây/nodes).
Module này giúp:

Hiển thị tất cả các node trong story.json

Vẽ đường liên kết giữa các node qua thuộc tính "target" của mỗi choice

Cho phép người dùng click vào node để xem thông tin

Hỗ trợ cho Story Builder UI và Test Story

Đây là bước để chuẩn bị cho Story Editor và Gameplay Debugger.

📦 Đầu ra

Tạo file JS mới:

/engine/mapRenderer.js


Module chứa các hàm:

✔ 1. loadStory(json)

Nhận JSON của toàn bộ story

Chuẩn hóa danh sách nodes

Tạo cấu trúc graph nội bộ

✔ 2. getMapData()

Trả về dữ liệu graph đơn giản để UI render:

{
  nodes: [{ id, x, y, title }],
  edges: [{ from, to }]
}

✔ 3. autoLayout()

Tự động bố trí vị trí x/y cho các node

Dùng thuật toán đơn giản: tree layout / grid layout / force layout mini
→ Yêu cầu AI khác hỗ trợ nâng cấp sau.

✔ 4. onNodeClick(id, callback)

Cho phép gán callback khi người dùng click node trong UI

🧠 Quy định kỹ thuật

Không viết UI trong task này

Không dùng canvas trực tiếp
→ Chỉ trả về data để UI xử lý

Toàn bộ liên kết được lấy từ:

nodes[id].choices[*].target

🔍 Ví dụ dữ liệu đầu ra
{
  "nodes": [
    { "id": "start", "title": "Mở đầu", "x": 100, "y": 50 },
    { "id": "A", "title": "Rẽ trái", "x": 100, "y": 200 },
    { "id": "B", "title": "Rẽ phải", "x": 300, "y": 200 }
  ],
  "edges": [
    { "from": "start", "to": "A" },
    { "from": "start", "to": "B" }
  ]
}

⚠️ Hạn chế

Không tạo UI

Không vẽ canvas

Không tạo editor
→ Task này chỉ chuẩn bị dữ liệu để Task 05–06 sử dụng.

🔥 Input để AI Writer (như ChatGPT, DeepSeek…) tạo code

Bạn có thể đưa cho AI khác prompt sau:

Hãy viết file /engine/mapRenderer.js theo các yêu cầu:

1. Hàm loadStory(json)
2. Hàm getMapData()
3. Hàm autoLayout()
4. Hàm onNodeClick(id, callback)

Yêu cầu:
- Không vẽ canvas
- Chỉ tạo dữ liệu nodes và edges
- Hỗ trợ auto-layout đơn giản
- Dữ liệu đầu ra dạng: { nodes: [...], edges: [...] }

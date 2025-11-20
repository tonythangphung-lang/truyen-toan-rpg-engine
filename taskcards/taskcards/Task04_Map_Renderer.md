🟩 Task 04 — MAP RENDERER (Bản đồ hiển thị node + đường liên kết)
🎯 Mục tiêu

Xây dựng module hiển thị bản đồ Story dạng graph (cây / mạng) để:

Hiện tất cả các node trong story.json

Vẽ đường liên kết giữa các node dựa vào choices.target

Cho phép người dùng click vào node để xem thông tin

Hỗ trợ Story Builder UI và Test Story

🧱 Chức năng chính
✔ 1. Hiển thị toàn bộ node

Mỗi node là 1 hình chữ nhật / circle

Hiện title

Hiện số lượng lựa chọn (choices count)

✔ 2. Vẽ đường nối giữa các node

Dựa vào:
choices[].target
Các đường nối dạng:

Mũi tên một chiều

Tự động cập nhật khi JSON thay đổi

✔ 3. Tự động bố trí bố cục (Auto Layout)

Force graph layout hoặc tree layout

Có mode "Grid" nếu muốn

Có thể zoom / pan

✔ 4. Tương tác người dùng

Khi click vào node:

Hiện chi tiết node

Cho phép Story Builder chọn node để chỉnh sửa

Cho phép Test Story nhảy đến node

📦 Output

File:
taskcards/Task04_Map_Renderer.md

Nội dung file cần:

Mục tiêu

Chức năng chính

Danh sách module JS cần

API cho Story Builder UI

Cách nhận dữ liệu (story.json) từ Core Engine

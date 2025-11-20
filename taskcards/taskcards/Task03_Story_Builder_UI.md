# Task 03 — STORY BUILDER UI (Trình tạo truyện trực quan)

## Mục tiêu
Xây dựng giao diện để:
- Tạo node mới
- Sửa node
- Kéo thả vị trí node trên bản đồ
- Thêm lựa chọn (choice)
- Thêm bài tập (exercise)
- Xuất file story.json đúng chuẩn schema của Task02

Story Builder là công cụ để:
- AI khác nhập nội dung
- Người dùng chỉnh sửa dễ dàng
- Tăng tốc sáng tác truyện

--------------------------------------------

## Chức năng UI cần có

### 1. Sidebar danh sách node
- Hiển thị toàn bộ node  
- Cho phép chọn 1 node để chỉnh sửa  
- Nút “+ Node mới”

### 2. Form chỉnh sửa Node
Các trường:
- title
- text
- media.img
- media.audio
- map.x
- map.y

### 3. Khu vực chọn Choice
Mỗi choice có:
- text
- description
- target (dropdown chọn node đích)
- condition.minScore
- condition.requiredItem
- exercise (có nút bật/tắt)

### 4. Popup tạo Exercise
- q (câu hỏi)
- a (đáp án)
- hint
- points

Nút: **Thêm / Lưu / Xóa**

### 5. Map Editor (mini canvas)
- Cho phép kéo thả node
- Thay đổi map.x, map.y theo vị trí kéo
- Zoom in / zoom out (tùy chọn)

### 6. Preview JSON
- Hiển thị phiên bản JSON đang được tạo
- Nút “Copy JSON”
- Nút “Export story.json”

--------------------------------------------

## Yêu cầu kỹ thuật

### 1. File output
Kết quả xuất về file:
- `/stories/<tên_truyện>.json`
- Tuân theo Task02 Story Schema

### 2. Không cần backend
- Chỉ cần HTML + CSS + JS thuần
- Lưu tạm data trong localStorage

### 3. Không viết core logic
→ Core chỉ nằm ở `/engine/core.js` (Task01)

UI chỉ tạo JSON.

--------------------------------------------

## Output cho AI khác

AI phải trả về:
- file `/ui/story_builder.html`  
- file `/ui/story_builder.js`  
- file `/ui/story_builder.css` (tùy chọn)
- Chạy độc lập, không lỗi console
- Có thể xuất JSON hợp lệ theo Task02

--------------------------------------------

## Các lỗi hay gặp cần tránh

1. Node không có ID cố định  
2. Trùng ID node  
3. Target không tồn tại  
4. map.x, map.y sai (ngoài 0–100)  
5. Ghi exercise thiếu trường  
6. JSON không parse được  
7. Không liên kết được giữa UI và JSON output

--------------------------------------------

## Tiêu chí hoàn thành
- Tạo được một story đơn giản với 5–7 nodes
- Xuất JSON hợp lệ và import ngược lại được
- Map Editor kéo thả hoạt động
- UI không lỗi khi reload trình duyệt

--------------------------------------------

## Mục tiêu cuối cùng
Tạo ra công cụ mạnh để:
- Người dùng tự sáng tác truyện
- AI nhiều mô hình hợp tác chung format JSON
- Tăng tốc sản xuất nội dung cho game


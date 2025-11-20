Task 01 — CORE ENGINE (Main Gameplay Runtime)
🎯 Mục tiêu

Xây dựng lõi vận hành của game truyện toán đa nhánh:

Điều khiển luồng story

Điều hướng scene

Xử lý lựa chọn

Khởi động bài tập khi người chơi chọn

Điểm số / level / mạng

Hệ thống lưu tiến trình

Đây là nền tảng quan trọng nhất của toàn bộ engine.

📦 Yêu cầu đầu ra

Tạo module JS mới:
/engine/core.js
Module này cần chứa các hàm:

✔ loadStory(json)

Load toàn bộ story từ file JSON

Chuẩn hóa dữ liệu nodes

Xác định node bắt đầu

✔ getCurrentNode()

Trả về node hiện tại trong story

✔ goToNode(id)

Chuyển sang node mới theo id

Kiểm tra node tồn tại

Ghi nhận lịch sử di chuyển nếu cần

✔ applyChoice(choice)

Nhận lựa chọn từ node hiện tại

Kiểm tra điều kiện (condition)

Nhảy sang node target

✔ startExercise(data)

Nhận bài tập toán

Trả dữ liệu về UI để render bài tập

✔ checkAnswer()

Nhận kết quả người chơi nhập

Chấm điểm

Update tiến trình

✔ saveProgress()

Lưu tiến trình cục bộ (localStorage)

✔ loadProgress()

Tải tiến trình đã lưu

Tự động đưa người chơi về node đã chơi gần nhất

🚫 Hạn chế

Trong Task 01, KHÔNG làm các phần sau:

Không viết giao diện UI

Không vẽ bản đồ

Không xử lý asset hình ảnh / âm thanh

Không tạo bài tập toán (để Task 10)

Task này chỉ quản lý logic, không hiển thị.

🤖 Input mẫu để AI khác tạo code Engine

Bạn có thể đưa nội dung sau cho AI cùng tham gia:
Hãy viết module /engine/core.js với các hàm:

- loadStory(json)
- getCurrentNode()
- goToNode(id)
- applyChoice(choice)
- startExercise(data)
- checkAnswer()
- saveProgress()
- loadProgress()

Yêu cầu:
- Không viết giao diện
- Không dùng HTML, CSS
- Chỉ xử lý logic story
- Story dạng JSON theo schema Task02


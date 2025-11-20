# Task 01 — CORE ENGINE (Main Gameplay Runtime)

## Mục tiêu
Xây dựng lõi vận hành của game truyện toán đa nhánh:
- Điều khiển luồng story
- Điều hướng scene
- Xử lý lựa chọn
- Khởi động bài tập khi người chơi chọn
- Điểm số / level / mạng
- Hệ thống lưu tiến trình

## Yêu cầu đầu ra
Tạo module JS mới: `/engine/core.js`
Chứa các hàm:

- loadStory(json)
- getCurrentNode()
- goToNode(id)
- applyChoice(choice)
- startExercise(data)
- checkAnswer()
- saveProgress()
- loadProgress()

## Hạn chế
- Không viết giao diện UI
- Không vẽ bản đồ
- Không xử lý asset

Core engine chỉ quản lý logic, không hiển thị.

## Input để AI làm việc
Bạn gửi cho AI:
- file core.js hiện tại nếu có
- story JSON mẫu
- mô tả flow gameplay

## Output AI phải trả về
- file core.js đầy đủ
- tài liệu hướng dẫn sử dụng
- danh sách lỗi tiềm năng


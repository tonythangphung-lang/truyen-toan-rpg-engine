🟥 Task 11 — ASSET LOADER (Trình tải hình ảnh, âm thanh, JSON)
🎯 Mục tiêu

Tạo hệ thống tải asset chuẩn mực để:

Tải hình ảnh cho story

Tải âm thanh cho scene hoặc chiến đấu

Tải JSON story

Cache kết quả để tăng tốc

🧱 Chức năng chính
✔ 1. Tải ảnh

Hàm:

loadImage(url): Promise<HTMLImageElement>


Kết quả:

Resolve khi tải xong

Reject khi lỗi

✔ 2. Tải âm thanh
loadAudio(url): Promise<HTMLAudioElement>

✔ 3. Tải JSON story
loadJSON(url): Promise<Object>


Dùng cho:

Story

Quest list

Items

Enemy stats

✔ 4. Cache hệ thống

Tất cả asset đã tải lưu vào:

assetCache = {
  images: {},
  audio: {},
  json: {}
}


Khi gọi lại URL cũ → trả ngay, không tải lại.

✔ 5. Batch Loader (tải hàng loạt)

Ví dụ:

loadAssets({
  images: ["hero.png", "bg.jpg"],
  audio: ["battle.mp3"],
  json: ["story.json"]
})


Return:

Tổng số asset

Số asset đã tải

Tiến độ (%)

📦 Output file

taskcards/Task11_Asset_Loader.md

Nội dung:

Mục tiêu

API load image/audio/json

Cache system

Batch loader

JSON ví dụ

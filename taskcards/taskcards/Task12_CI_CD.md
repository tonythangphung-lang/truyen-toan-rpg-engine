🟨 Task 12 — CI/CD (Tự động build → test → deploy)
🎯 Mục tiêu

Giúp dự án của bạn chạy tự động:

Kiểm tra code khi commit

Tạo bản build HTML tự động

Tự động deploy lên GitHub Pages

Đảm bảo toàn bộ engine luôn hoạt động

🧱 Chức năng chính
✔ 1. Thiết lập GitHub Actions

Tạo file:

.github/workflows/deploy.yml

Nội dung cơ bản:

Kiểm tra syntax JS

Build dự án

Deploy lên GitHub Pages

✔ 2. Tự động chạy khi bạn push code

Trigger:

on:
  push:
    branches: [ "main" ]

✔ 3. Script build

Dùng:

NodeJS

Rollup hoặc Vite

Build output vào:

/dist

✔ 4. Deploy lên GitHub Pages

Tự động upload folder /dist lên pages branch.

Sau đó bạn có link:

https://ten-github.github.io/truyen-toan-rpg-engine/

✔ 5. Chạy test tự động

Tạo file test:

/tests/core.test.js
/tests/exercise.test.js
/tests/storyLoader.test.js


GitHub Actions sẽ chạy test trước khi build.

📦 Output file

taskcards/Task12_CI_CD.md

Nội dung:

Mục tiêu

GitHub Actions

Build script

Deploy Pages

Unit tests

Cấu trúc thư mục

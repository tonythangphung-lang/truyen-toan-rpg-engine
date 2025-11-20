🟦 Task 09 — INVENTORY + ITEMS SYSTEM (Hệ thống vật phẩm)
🎯 Mục tiêu

Tạo hệ thống quản lý vật phẩm cho game RPG toán:

Thu thập vật phẩm

Trang bị item

Dùng item trong chiến đấu hoặc story

Buff chỉ số

Lưu tiến trình

🧱 Chức năng chính
✔ 1. Cấu trúc Item

Ví dụ JSON chuẩn:

{
  "id": "potion_small",
  "name": "Bình máu nhỏ",
  "type": "consumable",
  "effect": { "hp": +10 }
}


Các loại item:

consumable (dùng 1 lần)

equipment (vũ khí, áo giáp)

quest-item (phục vụ nhiệm vụ)

✔ 2. Inventory (túi đồ)

Lưu danh sách:

{
  "items": [
    { "id": "potion_small", "qty": 3 },
    { "id": "iron_sword", "qty": 1 }
  ]
}

✔ 3. Trang bị (Equipment)

Slot đề xuất:

weapon

armor

accessory

Khi trang bị:

atk + item.atk
def + item.def
hpMax + item.hpBonus

✔ 4. Dùng vật phẩm

Nếu consumable:

{
  "use": "potion_small",
  "result": { "hp": +10, "inventoryLeft": 2 }
}

✔ 5. Kết nối Quest System + Combat Math

Quest có thể yêu cầu item

Item có thể dùng trong Combat để hồi máu

Item drop sau trận đấu

📦 Output file

taskcards/Task09_Inventory_Items.md

Bao gồm:

Mục tiêu

Item structure

Inventory structure

Equipment

API: addItem, useItem, equipItem

JSON ví dụ

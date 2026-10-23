# 02 — CÂU LỆNH

## Năm mode

| Gõ | Nhận lại |
|---|---|
| `MODE 1 — nghiên cứu từ khoá cho <dịch vụ>, vùng <V1/V2>` | File JSON `markets/` → chạy generator ra `.xlsx` 5 sheet |
| `MODE 2 — sinh mẫu quảng cáo cho từ khoá <X>, chặng <S4>` | 15 headline + 4 description + 3–5 biến thể Meta + bảng chấm 14 điểm |
| `MODE 3 — dựng landing cho cụm <X>, chặng <S4>` | Copy-deck 14 khối theo khung L1–L5 |
| `MODE 4 — chẩn đoán` + dán số liệu | Tầng rò + 3 việc xếp theo thiệt hại |
| `MODE 5 — nội dung để AI trích dẫn` | Nội dung EN theo trang đích + cách đo Share of Voice |

⛔ **Thiếu `vùng` thì không chạy mode nào.** Không biết khách ở đâu thì không biết họ có đến được không.

---

## Câu hỏi vận hành hỏi thẳng được

```
Tuần này lead nhiều mà lịch hẹn không tăng. Vì sao?
```
```
CPL tuần này rẻ hơn tuần trước 30%. Đây là tin tốt hay tin xấu?
```
```
Nên mở rộng sang Quezon City không? Dịch vụ nào thì đáng?
```
```
Khách hỏi "how long does it last" — mình đang trả lời ở đâu?
```
```
Ngân sách 150k peso/tháng nên chia thế nào giữa 6 dịch vụ?
```
```
Mẫu quảng cáo này có qua được chính sách Meta không?
```

---

## Lệnh nửa tay

```bash
# sinh 1 bộ
python tools/build_keyword_workbook.py markets/threadlift-v1-bgc.json

# sinh tất cả các bộ
python tools/build_keyword_workbook.py "markets/*.json" -o out/

# gộp tri thức khi nền tảng chặn số file
python tools/gop-tham-khao.py
```

---

## Bốn cổng generator tự chặn

| Cổng | Chặn gì | Ví dụ thông báo lỗi |
|---|---|---|
| **GEO-TARGET** | Thiếu `market` hoặc `geo_mode` | `từ khoá #3: thiếu geo_mode` |
| **CLAIM** | `thong_diep` chứa claim cấm | `còn claim đã gỡ "written guarantee"` |
| **TỪ CẤM** | Từ cấm quảng cáo y tế | `thông điệp chứa từ cấm quảng cáo y tế` |
| **TRÙNG LẶP** | Trùng (từ khoá × khớp × **market**) | `trùng từ khoá x kiểu khớp x market` |

Trượt cổng nào → **không xuất file**, in đúng dòng lỗi.

⚠️ Cổng TRÙNG LẶP tính cả `market` là **có chủ ý**: cùng một chuỗi từ khoá ở V1 và V2 là **hai người khác nhau**, cần bid và landing khác. Bản KN-QT chỉ tính (từ khoá × khớp) nên báo nhầm — gói này đã sửa.

---

## Khi agent trả lời sai

| Dấu hiệu | Gõ |
|---|---|
| Quên cổng GEO | `Bạn chưa khai geo_mode. Làm lại, mọi dòng phải là Presence.` |
| Bịa giá hoặc số buổi | `Con số đó lấy từ đâu? Chưa có thì ghi [CHỜ XÁC NHẬN].` |
| Mẫu S4 không trả lời rào BỀN | `Mẫu S4 phải nêu số buổi và tổng chi phí. Chấm lại tiêu chí ⑭.` |
| Tư vấn bằng CPL | `Đo bằng chi phí/khách đến khám. CPL chỉ để chẩn đoán.` |
| Gợi ý dịch vụ ngoài phạm vi | `Ngoài 6 dịch vụ. Xem lỗi ② hồ sơ thương hiệu.` |
| Viết Taglish gượng | `Dùng English đi. Không có người bản địa duyệt thì giọng giả còn hại hơn.` |

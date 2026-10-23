# PROMPT — MODE 1 · NGHIÊN CỨU BỘ TỪ KHOÁ

> Đầu ra: **một file JSON** trong `markets/` → chạy generator ra **`.xlsx` 5 sheet**.
> Tri thức: `kn-vung-philippines.md` · `kn-chan-dung-hanh-trinh-ph.md` · `kn-cong-win-tu-khoa-ph.md`.

---

## Khối lệnh

```
MODE 1 — nghiên cứu bộ từ khoá.

VÙNG     : V1 (BGC · McKinley Hill · Taguig)
DỊCH VỤ  : Xline Thread Lift
NGÂN SÁCH: ₱150.000/tháng  (giả định, chưa chốt)

Làm theo đúng K1→K8, không đảo:
K1 vùng → K2 chân dung → K3 chặng S1–S6 → K4 chiến dịch
K5 landing → K6 từ khoá → K7 phủ định → K8 ngưỡng

Yêu cầu:
- 4–7 chân dung, mỗi chân dung có insight viết BẰNG LỜI KHÁCH trong ngoặc kép,
  ghi rõ người gõ có phải người điều trị không và thuộc vành đai nào.
- Phải có ít nhất một chân dung "đã làm ở nơi khác, không hài lòng".
- Mỗi dòng từ khoá khai market (V1–V4) và geo_mode = Presence.
- Chấm cổng WIN 4 tiêu chí, chỉ đưa vào file những từ ≥ 3/4.
- Ngân sách: S4 ≥ 20%, S3 ≥ 15%, S5 ≥ 30%, V1+V2 ≥ 70%.
- Xuất ra JSON đúng schema markets/README.md.

Cuối output liệt kê [CHỜ XÁC NHẬN] còn thiếu.
```

---

## Sau khi có JSON

```bash
python tools/build_keyword_workbook.py markets/<ten-file>.json
```

Generator chặn bốn cổng: GEO-TARGET · CLAIM · TỪ CẤM · TRÙNG LẶP. Trượt cổng nào thì **không xuất file** và in ra đúng dòng lỗi — sửa JSON rồi chạy lại.

---

## Ba lỗi hay gặp khi viết JSON

| Lỗi | Dấu hiệu | Sửa |
|---|---|---|
| Viết `insight` bằng lời marketing | *"Khách quan tâm giải pháp trẻ hoá không xâm lấn"* | Viết lại bằng câu khách nói: *"Tôi chưa muốn phẫu thuật, tôi chỉ muốn nhìn đỡ mệt mỏi hơn"* |
| `market` ghi theo thành phố trong từ khoá | `tu_khoa: "thread lift taguig"` → `market: "Taguig"` | `market` là **người gõ đang ở đâu** → `V1` hoặc `V2` |
| `ty_trong` không cộng thành 1.0 | Generator báo lỗi | Rà lại, tổng phải đúng 1.0 |

---

## Thêm bộ mới cho dịch vụ khác

Một bộ = **một vùng × một dịch vụ**. Sáu dịch vụ × hai vùng chủ lực = tối đa 12 bộ, nhưng ⛔ **đừng dựng hết một lúc**.

Thứ tự đề xuất:
1. `threadlift-v1-bgc` — giá trị ca cao nhất, đã có ✅
2. `melasma-v1-bgc` — liệu trình nhiều buổi, rào BỀN rõ nhất
3. `mesohair-v1-bgc` — rào riêng tư mạnh, cạnh tranh thấp
4. `threadlift-v2-makati` — mở rộng vùng sau khi V1 ổn định

⛔ Không dựng bộ `acne` trước — giá trị ca thấp nhất, và nhóm khách trẻ nhạy giá nhất.

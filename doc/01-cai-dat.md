# 01 — CÀI ĐẶT (20 phút)

Agent này có **hai nửa**:
- **Nửa não** — prompt + knowledge, chạy trên Claude / ChatGPT / Gemini. Không cần cài gì lên máy.
- **Nửa tay** — `tools/build_keyword_workbook.py`, biến file JSON thành Excel 5 sheet. Cần Python + `openpyxl`.

---

## 0. Ba ô phải điền khi tạo agent mới

**Tên**
```
Agent-AdsOptimize-Phi
```

**Mô tả** — 247 ký tự, dưới trần 300 của ChatGPT:
```
Nghiên cứu từ khoá, sinh mẫu quảng cáo, dựng landing và chẩn đoán chỉ số cho phòng khám thẩm mỹ Sunwoo tại Taguig, Philippines. Chia theo vành đai đi lại, tối ưu theo chi phí mỗi khách đến khám, rà luật quảng cáo y tế PH trước mọi output.
```

**Câu mở đầu hội thoại**
```
MODE 1 — nghiên cứu bộ từ khoá cho Thread Lift, vùng V1 (BGC)
```
```
MODE 4 — tuần này lead nhiều mà lịch hẹn không tăng, vì sao?
```

---

## 1. Nạp bộ não

| Nền tảng | Dán vào đâu | Dùng file nào |
|---|---|---|
| **Claude Project** | *Custom instructions* | [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md), khối giữa hai vạch ▼▲ |
| **ChatGPT Custom GPT** | *Instructions* (trần 8.000 ký tự) | [`SYSTEM-PROMPT-NGAN.md`](../SYSTEM-PROMPT-NGAN.md) — hiện **7.448** ký tự |
| **Gemini Gem** | *Chỉ dẫn* | `SYSTEM-PROMPT.md` |
| **Claude Code** | `CLAUDE.md` hoặc dán vào chat | `SYSTEM-PROMPT.md` |

## 2. Nạp tri thức

**Bản rời (14 file)** — chuẩn:
```
knowledge/kn-ho-so-thuong-hieu-sunwoo.md   prompts/prompt-nghien-cuu-tu-khoa.md
knowledge/kn-vung-philippines.md           prompts/prompt-build-ad-set.md
knowledge/kn-chan-dung-hanh-trinh-ph.md    prompts/prompt-build-landing-page.md
knowledge/kn-rao-phap-ly-ph.md             prompts/prompt-quy-trinh-tron-goi.md
knowledge/kn-cong-win-tu-khoa-ph.md        prompts/prompt-geo-answer.md
knowledge/kn-engine-win-ad-ph.md           markets/README.md
knowledge/kn-khung-landing-ph.md
knowledge/kn-chan-doan-chi-so-ph.md
knowledge/kn-quy-trinh-tuan-ph.md
```

**Bản gộp (2 file)** — khi nền tảng chặn số file (Gemini Gems: 10):
```
goi/GOP-tri-thuc.md   goi/GOP-prompt.md
```
Sinh lại sau mỗi lần sửa: `python tools/gop-tham-khao.py`. ⛔ Đừng sửa tay file gộp.

---

## 3. Cài nửa tay

```bash
pip install openpyxl
python tools/build_keyword_workbook.py markets/threadlift-v1-bgc.json
```

Ra file `out/PHI _ Google Ads _ ThreadLift V1 BGC.xlsx` — 5 sheet: Tổng quan · Bộ từ khoá · Từ khoá phủ định · Hành trình KH · Giá thầu & Tối ưu.

**Generator là brand-neutral.** Tên thương hiệu, đơn vị tiền tệ và danh sách claim cấm riêng đều đọc từ file JSON (`zone.thuong_hieu` · `zone.don_vi_tien` · `zone.claim_cam`), ⛔ không hardcode. Dùng lại được cho phòng khám khác.

**Thử cổng chặn:** sửa một `geo_mode` thành `Interest` rồi chạy lại — generator phải **dừng**, không xuất file. Dừng đúng là cổng còn sống.

---

## 4. ⚠️ Bốn việc phải làm xong TRƯỚC khi tiêu đồng đầu tiên

| # | Việc | Ai | Chặn gì nếu thiếu |
|---|---|---|---|
| 1 | Xác nhận **phạm vi giấy phép** của cơ sở bằng văn bản | Pháp chế | ⛔ **Chặn tất cả** |
| 2 | Số đăng ký FDA PH của thiết bị/sản phẩm | Pháp chế | MODE 2 · 3 |
| 3 | **Giá và số buổi** từng dịch vụ | Phòng khám + bác sĩ | MODE 1 · 2 · 3 |
| 4 | Xoá **lỗi ① và ②** trên trang production | Marketing | ⛔ Không xuất mẫu nào dẫn về trang đó |

Lỗi ① = *"300++ Board-certified doctors"* trong khi site chỉ nêu 2 bác sĩ.
Lỗi ② = FAQ nói có *"dental, plastic surgery"* nhưng dịch vụ công bố chỉ là da liễu – thẩm mỹ nội khoa.
Chi tiết: [`knowledge/kn-ho-so-thuong-hieu-sunwoo.md`](../knowledge/kn-ho-so-thuong-hieu-sunwoo.md) §6.

---

## 5. Checklist 12 ô trước khi bật chiến dịch

Nằm ở [`knowledge/kn-quy-trinh-tuan-ph.md`](../knowledge/kn-quy-trinh-tuan-ph.md) §2. Hai nhóm quan trọng nhất:

- **Ô 5–6 GEO** — mọi chiến dịch đặt `Presence` / *People living in this location*. Đây là lỗi im lặng, đắt nhất của gói này.
- **Ô 7 tag CRM** — gắn `vung` · `dich_vu` · `chang` từ **ngày đầu**. Việc 30 phút ở tuần 1, hoặc là việc không bao giờ làm được nữa.

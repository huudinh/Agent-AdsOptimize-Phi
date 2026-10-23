# CHANGELOG

## v1.0 — 2026-10-23
Bản đầu. Tham khảo kiến trúc [`Agent-AdsOptimize-Kangnam-QT`](../../Agent-AdsOptimize-Kangnam-QT/), **không phải bản dịch** — xem bảng khác biệt ở cuối `SYSTEM-PROMPT.md`.

**Nguồn dữ liệu thương hiệu:** <https://sunwooaesthetic.ph/> đọc ngày 2026-10-23.

**Có gì**
- Bộ não `SYSTEM-PROMPT.md` (19 §) + `SYSTEM-PROMPT-NGAN.md` (**7.448** ký tự, vừa trần 8.000 của ChatGPT).
- 9 module tri thức trong `knowledge/`.
- 5 prompt mẫu trong `prompts/`.
- 1 bộ market hoàn chỉnh `markets/threadlift-v1-bgc.json` — 5 chân dung · 5 chiến dịch · 5 landing · 17 từ khoá, **đã build ra `.xlsx` 5 sheet**.
- Generator và bundler đã **tách khỏi thương hiệu**.

**Năm thứ thay đổi logic so với gói KN-QT**

| Thay đổi | Vì sao |
|---|---|
| Tầng **quốc gia → vành đai đi lại V1–V4** | Phòng khám nội địa một cơ sở; khách tự đến. Metro Manila đo bằng **phút kẹt xe**, không bằng km |
| Rào **XA → BỀN** | Thủ thuật không phẫu thuật, nhiều buổi, có thời hạn. Câu quyết định là *"được bao lâu rồi lại phải trả tiếp"* |
| Chặng **S4 chuyến đi → S4 số buổi & tổng chi phí** | Chặng cạnh tranh thấp nhất của ngành này — cả ngành quảng cáo *"starts at X"*, không ai nói tổng |
| `geo_mode` **linh hoạt → luôn `Presence`** | Để nền tảng tự chọn = lead từ Cebu/Davao, CPL rẻ ảo, không ai đến khám |
| Pháp lý **VN + nước người xem → PH + nền tảng** | FDA RA 9711 · DOH · PRC · ASC · Data Privacy Act RA 10173 |

**Hai lỗi của generator KN-QT đã sửa trong gói này**

1. **Cổng CLAIM hardcode tri thức Kangnam.** `board certified` bị chặn cứng trong code — đúng với thị trường US/AU của gói đó, nhưng sai với gói này vì bác sĩ Sunwoo **có** chứng nhận thật (Diplomate PDS). → Chuyển thành `zone.claim_cam` trong JSON; code chỉ giữ danh sách rủi ro ở **mọi** thị trường.
2. **Cổng TRÙNG LẶP tính thiếu `market`.** Cùng một chuỗi từ khoá ở hai vùng là hai người khác nhau — chính README của KN-QT nói vậy, nhưng code lại báo trùng. → Khoá trùng lặp giờ gồm cả `market`.

Hai thay đổi này nên **đưa ngược về** gói KN-QT, vì đó là lỗi chung của generator chứ không phải khác biệt giữa hai gói.

**🔴 Sáu lỗi phát hiện trên trang production** — xem `kn-ho-so-thuong-hieu-sunwoo.md` §6. Hai lỗi đầu là **cổng chặn**: không xuất mẫu quảng cáo nào dẫn về trang còn lỗi ① và ②.

**Chưa có — việc của giai đoạn sau**
- `[CHỜ XÁC NHẬN]` 10 mục ở hồ sơ thương hiệu, trong đó **mục 4 (phạm vi giấy phép) chặn tất cả các mode**.
- Mới có 1/12 bộ market. Thứ tự dựng tiếp đề xuất ở `prompts/prompt-nghien-cuu-tu-khoa.md`.
- Chưa có khung landing HTML (gói KN-QT có `template/lp-skeleton-en.html`). Hiện mới có copy-deck.
- Nhóm N1 cộng đồng Hàn tại McKinley Hill: chưa mở, chờ xác nhận có nhân sự nói tiếng Hàn.
- Chưa có trang hướng dẫn web như các gói anh em.

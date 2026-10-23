# 🇵🇭 ADS OPTIMIZE — SUNWOO PHILIPPINES (PHI)

> Version 1.0 · AI **nghiên cứu bộ từ khoá · sinh mẫu quảng cáo · dựng landing · chẩn đoán chỉ số** cho **Sunwoo Aesthetic Center** — phòng khám thẩm mỹ K-beauty tại McKinley Hill, Taguig, Metro Manila.

Kiến trúc **BRAIN brand-neutral** ([`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md)) + **MODULE thương hiệu tách riêng** ([`knowledge/kn-ho-so-thuong-hieu-sunwoo.md`](knowledge/kn-ho-so-thuong-hieu-sunwoo.md)) → đổi phòng khám chỉ cần thay module.

**Site phục vụ:** <https://sunwooaesthetic.ph/>
Agent tham khảo kiến trúc: [`Agent-AdsOptimize-Kangnam-QT`](../Agent-AdsOptimize-Kangnam-QT/) — **đây không phải bản dịch**, xem bảng khác biệt bên dưới.

---

## ⚠️ Đọc trước: đây là phòng khám nội địa, không phải du lịch y tế

Gói KN-QT phục vụ khách **bay sang Việt Nam**. Gói này phục vụ khách **sống ở Metro Manila và tự lái xe tới McKinley Hill**.

⛔ Mọi tri thức về visa · số ngày ở lại · đón sân bay · phiên dịch · so sánh quốc gia — **không áp dụng**. Một landing nói về đón sân bay gửi cho một phụ nữ đang ở Makati là một landing hỏng.

| | KN-QT | **PHI** |
|---|---|---|
| Mô hình | Du lịch y tế | **Phòng khám nội địa** |
| Phân tầng | Quốc gia · kiều bào · expat | **Bán kính đi lại V1–V4** |
| Rào thứ tư | **XA** *"về nhà ai lo cho tôi"* | **BỀN** *"hết tác dụng rồi tôi trả tiếp bao nhiêu"* |
| Chặng đặc thù | S4 Kế hoạch chuyến đi | **S4 Số buổi & tổng chi phí** |
| `geo_mode` | Presence+Interest theo tầng | ⛔ **Presence, luôn luôn** |
| Dịch vụ | Đại phẫu, một lần | **Không phẫu thuật, nhiều buổi, có thời hạn** |
| Kênh | Search-first | **Meta-first** |

**Bốn thứ giữ nguyên vì là phương pháp, không phải nội dung:** kiến trúc BRAIN + module thương hiệu · 5 mode · schema JSON → generator Excel · đo bằng **chi phí/khách đến khám**.

---

## Nguyên tắc tối thượng

> **Chỉ số trục là `chi phí / khách ĐẾN KHÁM`.** CPL chỉ để chẩn đoán.
>
> CPL là chỉ số gây hiểu lầm nhất của gói này: mở rộng geo ra cả nước làm CPL rẻ đi ngay, và **không ai trong số lead mới đến khám được**. Một chiến dịch CPL đẹp mà không ai tới phòng khám là một chiến dịch thất bại.

> **Agent chỉ GỢI Ý, người duyệt trước khi chạy.** AI không bật/tắt chiến dịch và không tiêu tiền.

---

## Năm mode

| Mode | Làm gì | Input tối thiểu | Đầu ra |
|---|---|---|---|
| **1 · KEYWORD-RESEARCH** | 1 **vùng × dịch vụ** → bộ từ khoá theo chặng | **vùng** + dịch vụ + ngân sách | JSON `markets/` → **`.xlsx` 5 sheet** |
| **2 · WIN-AD** | Từ khoá → mẫu quảng cáo | từ khoá + **vùng** + chặng | 15 headline + 4 description + 3–5 biến thể Meta + **bảng chấm 14 điểm** |
| **3 · LDP-BUILD** | Cụm từ khoá → landing L1–L5 | cụm + **vùng** + chặng | copy-deck 14 khối |
| **4 · OPTIMIZE** | Số liệu → chẩn đoán | số liệu **cắt theo vùng** | tầng rò + 3 việc xếp theo thiệt hại |
| **5 · GEO-ANSWER** | Nội dung để AI trích dẫn | cụm câu hỏi | nội dung EN + cách đo Share of Voice |

⛔ **Thiếu `vùng` thì không chạy mode nào.**

---

## ⚠️ Cổng GEO — ràng buộc cứng, và là lỗi im lặng đắt nhất

Phòng khám có **một cơ sở**. Khách phải **đến tận nơi**. Vì vậy:

⛔ **MỌI từ khoá, MỌI chiến dịch: `geo_mode = Presence`** (Meta: *People living in this location*).

Để nền tảng tự chọn (`Presence or interest` là mặc định) → quảng cáo hiện cho người ở Cebu, Davao, nước ngoài. **CPL rẻ đi rõ rệt, và không ai đến khám.**

> Nền tảng **không cảnh báo**. Lỗi hiện ra sau 6–10 tuần dưới dạng: *"lead nhiều mà lịch hẹn không tăng"* — và lúc đó cả đội sẽ đi đổ lỗi cho người trực page.

**Kiểm ở 4 chỗ:** §4 bộ não · cột `geo_mode` mọi dòng từ khoá · tiêu chí ⑦ bảng chấm 14 điểm · cổng GEO-TARGET trong generator.

---

## Bốn vành đai — phân tầng thật của gói này

Metro Manila không đo bằng kilômét, đo bằng **phút kẹt xe**.

| Tầng | Khu vực | Tới McKinley Hill | Ý nghĩa |
|---|---|---|---|
| **V1 Lõi** | BGC · McKinley Hill · Taguig | 5–15' | Bid cao nhất, đi khám buổi trưa được |
| **V2 Kề** | Makati · Pasay · Mandaluyong · Pasig | 20–45' | Chủ lực khối lượng, cần lý do đủ mạnh để vượt EDSA |
| **V3 Xa trong Metro** | QC · Manila · Parañaque · Alabang | 45–90' | ⚠️ **Chỉ dịch vụ giá trị ca cao** |
| **V4 Ngoài Metro** | Cavite · Laguna · tỉnh khác | 90'+ | ⛔ **Mặc định LOẠI** |

**Ngân sách V1 + V2 ≥ 70%.** Đây không phải quy tắc tiết kiệm — đây là quy tắc *đi lại có thật*.

**Ba nhóm cắt ngang vành đai:** ★ cộng đồng **Hàn Quốc tại McKinley Hill** (ngay cạnh phòng khám, định vị K-beauty khớp hoàn toàn, gần như chưa ai chạy riêng) · expat/văn phòng BGC · OFW và gia đình.

---

## Rào cản thứ tư: **BỀN**

Nội địa VN có **SỢ · NGỜ · NGẠI**. Quốc tế thêm **XA**. Gói này thêm **BỀN**.

> *"Được bao lâu rồi lại phải làm tiếp? Tôi phải trả tiền này mãi à?"*

Ba rào đầu là rào **trước khi làm**. BỀN là rào **sau khi đã muốn làm** — khách đã tin bác sĩ, đã chấp nhận giá một buổi, rồi mới nghĩ tới năm sau. Mất khách ở đây là đắt nhất.

Và đây là rào **cả ngành né tránh**: ai cũng quảng cáo *"starts at ₱X"* cho một buổi, không ai nói tổng. Khách biết vậy, nên họ mặc định **không tin con số trong quảng cáo**.

> **Phép thử trước khi xuất bất kỳ mẫu hay landing nào:**
> *"Đọc xong, khách có tính được mình tốn bao nhiêu trong 12 tháng tới không?"* Chưa → chưa xong.

---

## Phễu 6 chặng — chặng quyết định là **S4**

| Chặng | Dấu hiệu | Rào | Landing | Ads? |
|---|---|---|---|---|
| S1 Nhận biết | `what is` | — | — | ❌ |
| S2 So sánh cách làm | `vs` · `worth it` | NGỜ | **L1** | ✅ bid thấp |
| S3 Nỗi sợ & an toàn | `side effects` · `gone wrong` | **SỢ** | **L2** | ✅ |
| **S4 Số buổi & tổng chi phí ★★** | `how many sessions` · `how long does it last` · `maintenance` | **BỀN** | **L3** | ✅ **ưu tiên** |
| S5 Chọn nơi làm | `bgc` · `near me` · `book` | NGẠI | **L4** | ✅ bid cao nhất |
| S6 Sau điều trị | `aftercare` | BỀN | Trang CRM | ❌ |

**S4 có cạnh tranh thấp nhất trong cả phễu.** Đối thủ đổ tiền vào từ khoá giá và từ khoá chọn nơi; gần như không ai làm trang trả lời *"how many sessions"*. Người gõ S4 có ý định mua cao hơn người gõ S2 nhưng giá thầu rẻ hơn người gõ S5.

**Ngân sách: S4 ≥ 20% · S3 ≥ 15% · S5 ≥ 30%.**

---

## 🔴 Sáu lỗi đang có trên trang production — phát hiện 2026-10-23

| # | Lỗi | Sửa |
|---|---|---|
| ① | **"300++ Board-certified doctors"** trong khi site chỉ nêu **2 bác sĩ** | Đổi sang con số đếm được |
| ② | **FAQ nói có "dental, plastic surgery"** nhưng dịch vụ công bố chỉ là da liễu – thẩm mỹ | Xác nhận phạm vi giấy phép, chưa xác nhận thì **xoá** |
| ③ | **"Written guarantee"** cho kết quả thẩm mỹ y khoa | Đổi sang bảo đảm **quy trình**, có T&C văn bản |
| ④ | **"#1 K-beauty Medical Aesthetic Center in Philippines"** | Tuyên bố tối cao cần bằng chứng chuẩn ASC |
| ⑤ | Lời chứng thực nêu tên + ảnh trước/sau | Giữ trên web nếu hợp lệ, ⛔ không bê vào creative quảng cáo |
| ⑥ | Kênh chat đẩy **WhatsApp** | Ở PH **Messenger/Viber** mới phổ biến. Đo 4 tuần rồi đổi thứ tự nút |

> **Lỗi ① và ② là cổng chặn.** ⛔ Không xuất mẫu quảng cáo nào dẫn về trang còn hai lỗi này — tiền đổ vào một trang tự mâu thuẫn là tiền mất, và lỗi ② có thể thành vấn đề giấy phép.

---

## Chín module tri thức

| File | Nội dung |
|---|---|
| [`kn-ho-so-thuong-hieu-sunwoo`](knowledge/kn-ho-so-thuong-hieu-sunwoo.md) | **Module thương hiệu** — 6 dịch vụ · 2 bác sĩ · 6 lỗi production · 10 mục `[CHỜ XÁC NHẬN]` |
| [`kn-vung-philippines`](knowledge/kn-vung-philippines.md) | 4 vành đai · 3 nhóm đặc thù · Taglish · kênh PH · mùa vụ · payday |
| [`kn-chan-dung-hanh-trinh-ph`](knowledge/kn-chan-dung-hanh-trinh-ph.md) | 4 rào cản · phễu S1–S6 · 6 chân dung gốc · micro-conversion |
| [`kn-rao-phap-ly-ph`](knowledge/kn-rao-phap-ly-ph.md) | **Cổng chặn** — FDA/DOH/PRC/ASC/NPC · checklist 12 ô · chính sách Meta & Google |
| [`kn-cong-win-tu-khoa-ph`](knowledge/kn-cong-win-tu-khoa-ph.md) | Cổng WIN 4 tiêu chí · phủ định 3 lớp · quy tắc khớp |
| [`kn-engine-win-ad-ph`](knowledge/kn-engine-win-ad-ph.md) | B1→B7 · **bảng chấm 14 điểm** · 10 công thức headline |
| [`kn-khung-landing-ph`](knowledge/kn-khung-landing-ph.md) | Khung L1–L5 · 14 khối · ★ dựng chi tiết L3 |
| [`kn-chan-doan-chi-so-ph`](knowledge/kn-chan-doan-chi-so-ph.md) | Phễu 7 tầng · 3 tag CRM · bảng triệu chứng · lộ trình 3 pha |
| [`kn-quy-trinh-tuan-ph`](knowledge/kn-quy-trinh-tuan-ph.md) | Nhịp tuần · **checklist 12 ô trước khi bật** · phân vai |

---

## Quick start (5 bước)

1. Tạo 1 Project / GPT / Gem mới. Tên và mô tả: [`doc/01-cai-dat.md`](doc/01-cai-dat.md) §0.
2. **Instructions:** dán khối ▼▲ trong [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) — riêng **ChatGPT** dùng [`SYSTEM-PROMPT-NGAN.md`](SYSTEM-PROMPT-NGAN.md) (7.448/8.000 ký tự).
3. **Knowledge:** upload 14 file bản rời, hoặc 2 file trong [`goi/`](goi/) nếu nền tảng chặn số file.
4. Cài nửa tay: `pip install openpyxl`.
5. Chạy thử: `python tools/build_keyword_workbook.py markets/threadlift-v1-bgc.json`

**Câu lệnh mẫu:**
```
MODE 1 — nghiên cứu bộ từ khoá cho Melasma (PicoSure Pro), vùng V1.
Ngân sách giả định ₱150k/tháng. Làm theo K1→K8.
```
```
Tuần này lead tăng 40% mà lịch hẹn không đổi. Số liệu đây. Vì sao?
```

---

## Nửa tay — generator brand-neutral

```bash
python tools/build_keyword_workbook.py markets/threadlift-v1-bgc.json
python tools/build_keyword_workbook.py "markets/*.json" -o out/
python tools/gop-tham-khao.py      # gộp tri thức
```

Tên thương hiệu, đơn vị tiền tệ và claim cấm riêng đọc từ JSON (`zone.thuong_hieu` · `don_vi_tien` · `claim_cam`), ⛔ không hardcode — dùng lại được cho phòng khám khác.

**Bốn cổng generator tự chặn:** GEO-TARGET · CLAIM · TỪ CẤM · TRÙNG LẶP (tính cả `market`). Trượt cổng nào → **không xuất file**.

⚠️ **Hai lỗi của generator KN-QT đã sửa ở đây** và nên đưa ngược về gói đó — xem [`doc/CHANGELOG.md`](doc/CHANGELOG.md).

---

## ⚠️ Bốn việc phải xong trước khi tiêu đồng đầu tiên

1. 🔴 **Phạm vi giấy phép** của cơ sở, bằng văn bản — ⛔ thiếu thì chặn tất cả các mode.
2. 🔴 **Số đăng ký FDA PH** của thiết bị và sản phẩm.
3. **Giá và số buổi** từng dịch vụ — thiếu thì không chạy được MODE 1/2/3.
4. **Xoá lỗi ① và ②** trên trang production.

Danh sách đầy đủ 10 mục: [`knowledge/kn-ho-so-thuong-hieu-sunwoo.md`](knowledge/kn-ho-so-thuong-hieu-sunwoo.md) §8.

---

## Tài liệu
| File | Nội dung |
|---|---|
| [`doc/01-cai-dat.md`](doc/01-cai-dat.md) | Cài đặt · nạp tri thức · 4 việc phải làm trước |
| [`doc/02-cau-lenh.md`](doc/02-cau-lenh.md) | 5 mode · câu hỏi vận hành · khi agent trả lời sai |
| [`markets/README.md`](markets/README.md) | Schema JSON 18 khối · 4 cổng generator |
| [`doc/CHANGELOG.md`](doc/CHANGELOG.md) | Khác biệt so với KN-QT · những gì chưa có |

---

## Ranh giới

Agent này **không**: bật/tắt chiến dịch · tiêu tiền · phát ngôn y khoa · chẩn đoán · cam kết kết quả · quảng cáo dịch vụ ngoài 6 dịch vụ đã công bố.

⚠️ **File pháp lý là hướng dẫn vận hành, không phải tư vấn pháp lý.** Mọi mục 🔴 phải được pháp chế hoặc luật sư của phòng khám xác nhận trước khi chạy tiền thật. Quy định PH và chính sách nền tảng **đổi theo thời điểm** — tra lại trước mỗi quý.
"# Agent-AdsOptimize-Phi" 

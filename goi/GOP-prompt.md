# PROMPT MẪU PHI — Ads Optimize Sunwoo Philippines
> File này gộp **5 prompt mẫu** từ `prompts/`. Sinh tự động ngày 2026-10-23 bằng `python tools/gop-tham-khao.py`.
> ⛔ **Không sửa file này** — sửa ở bản rời trong thư mục nguồn rồi chạy lại lệnh trên.

**Cách đọc:** mỗi phần bắt đầu bằng dòng `===== tên file =====` và là **một đơn vị tri thức riêng**. Tham chiếu dạng `[[tên-file]]` trong văn bản trỏ tới **phần cùng tên ngay trong file này**, không phải file bên ngoài.

## MỤC LỤC

| # | File | Cỡ |
|---|---|---|
| 1 | `prompt-build-ad-set.md` | 2.2 KB |
| 2 | `prompt-build-landing-page.md` | 2.4 KB |
| 3 | `prompt-geo-answer.md` | 2.6 KB |
| 4 | `prompt-nghien-cuu-tu-khoa.md` | 2.7 KB |
| 5 | `prompt-quy-trinh-tron-goi.md` | 2.8 KB |


===== prompt-build-ad-set.md =====

# PROMPT — MODE 2 · SINH MẪU QUẢNG CÁO

> Tri thức: `kn-engine-win-ad-ph.md` · `kn-rao-phap-ly-ph.md` · `kn-chan-dung-hanh-trinh-ph.md`.

---

## Khối lệnh

```
MODE 2 — sinh mẫu quảng cáo.

TỪ KHOÁ  : how long does thread lift last
VÙNG     : V1
DỊCH VỤ  : Xline Thread Lift
CHẶNG    : S4
CHÂN DUNG: CD1
RÀO      : BỀN
KÊNH     : Google Search + Meta

Làm theo B1→B7. Yêu cầu:
- Google: 15 headline (<=30 ky tu) chia theo 5 vai tro x 3, 4 description (<=90).
- Meta: 3-5 bien the, primary text bang TAGLISH, headline English chuan.
- Cham bang 14 diem, in ra bang.
- Ra 12 o phap ly.
- Cuoi output: khoi CLAIM CAN PHAP CHE DUYET.

Mau S4 BAT BUOC tra loi rao BEN: so buoi + tong chi phi + giu bao lau.
Chua co so that thi ghi [CHO XAC NHAN], KHONG bia so.
```

---

## Đọc bảng chấm

| Điểm | Nghĩa |
|---|---|
| ⑦ hoặc ⑩ = 0 | **LOẠI THẲNG**, không tính tổng |
| < 10/14 | Viết lại, không chạy |
| 10–11 | Chạy được, ghi rõ tiêu chí thiếu |
| ≥ 12 | Ưu tiên ngân sách |

⚠️ Tiêu chí **⑭ trả lời rào BỀN** là bắt buộc với mọi mẫu S4. Mẫu S4 không nêu được số buổi và tổng chi phí thì nó chỉ là một mẫu S5 đặt nhầm chỗ.

---

## Ngôn ngữ theo kênh

| Kênh | Ngôn ngữ |
|---|---|
| Google Search · landing | **English chuẩn** |
| Meta · TikTok creative · kịch bản Messenger | **Taglish** |
| Nhóm Hàn McKinley Hill | **Tiếng Hàn** |

⛔ Không Taglish cho: tên dịch vụ y khoa · câu miễn trừ · thông tin giá · chỉ định điều trị.
⛔ Không có người bản địa duyệt Taglish thì dùng English — giọng giả còn hại hơn.

---

## Ba câu không được viết

```
⛔ "Nahihiya ka ba sa buhok mo?"        → chê ngoại hình người xem, Meta chặn
⛔ "Guaranteed results, 100% safe"       → cam kết tuyệt đối, trượt ô ② pháp lý
⛔ "The #1 K-beauty clinic in PH"        → tuyên bố tối cao, trượt ô ③
```

Chuyển mọi câu *"Bạn có đang bị…"* thành câu trần thuật về **dịch vụ**, không về **khuyết điểm của người xem**.


===== prompt-build-landing-page.md =====

# PROMPT — MODE 3 · DỰNG LANDING

> Tri thức: `kn-khung-landing-ph.md` · `kn-chan-dung-hanh-trinh-ph.md` · `kn-rao-phap-ly-ph.md`.

---

## Khối lệnh

```
MODE 3 — dung landing.

CUM TU KHOA : how long does thread lift last / how many sessions / package price
VUNG        : V1
DICH VU     : Xline Thread Lift
CHANG       : S4
CHAN DUNG   : CD1, CD3
RAO         : BEN

Chon khung theo CHANG. Xuat copy-deck theo tung khoi B01-B14,
ghi ro khoi nao bat buoc, khoi nao bo qua va vi sao.

Trang L3 BAT BUOC du ba khoi:
  B07 so buoi trong lieu trinh
  B08 tong chi phi - neu CA gia/buoi VA gia tron goi
  B09 giu bao lau + nhip duy tri + chi phi duy tri/nam

Cuoi output: phep thu BEN + khoi CLAIM CAN PHAP CHE DUYET.
```

---

## Chọn khung

| Chặng | Khung | Rào gỡ |
|---|---|---|
| S2 | **L1** So sánh cách làm | NGỜ |
| S3 | **L2** Trả lời thẳng | SỢ |
| **S4** | ★ **L3** Liệu trình & chi phí | **BỀN** |
| S5 | **L4** Đặt lịch | NGẠI |
| — | **L5** Cộng đồng Hàn | NGỜ |

⛔ Một trang gỡ một rào. ⛔ Không đổ mọi chiến dịch về trang chủ.

---

## Phép thử trước khi xuất

> **L3:** *"Đọc xong, khách có tính được mình tốn bao nhiêu trong 12 tháng tới không?"*
> **L2:** *"Đọc xong, khách có biết mình sẽ cảm thấy gì trong lúc làm không?"*
> **L4:** *"Đọc xong, khách có biết đỗ xe ở đâu và mấy giờ mở cửa không?"*

Chưa trả lời được → trang chưa xong.

---

## ⛔ Hai điều kiện chặn

1. **Chưa có `[CHỜ XÁC NHẬN]` mục 1–2** (giá và số buổi) → **không xuất L3**. Trang liệu trình điền số bịa còn tệ hơn không có trang.
2. **Trang production còn lỗi ① và ②** (300++ doctors · dental/plastic surgery trong FAQ) → ⛔ không xuất mẫu quảng cáo nào dẫn về đó.

---

## Kỹ thuật — ba thứ quyết định ở Philippines

| | Yêu cầu |
|---|---|
| **Tốc độ mobile** | LCP < 2,5s trên 4G trung bình |
| **Click-to-call nổi** | Nút gọi + Messenger dính đáy màn hình |
| **Chỉ đường + đỗ xe** | McKinley Hill khó tìm chỗ đỗ — đây là lý do huỷ hẹn có thật |

Form giữ đúng **4 trường** (tên · số · dịch vụ · khu vực), đặt **sau** phần gỡ rào, **micro-conversion trước form**.
⚠️ Đổi `Your area` thành **dropdown V1–V4**, nếu không MODE 4 không cắt được báo cáo theo vùng.


===== prompt-geo-answer.md =====

# PROMPT — MODE 5 · NỘI DUNG ĐỂ AI TRÍCH DẪN (GEO)

> Người Philippines ngày càng hỏi trợ lý AI trước khi hỏi Google. Mode này sản xuất nội dung tiếng Anh để **AI trích dẫn phòng khám** khi trả lời những câu đó.

---

## Khối lệnh

```
MODE 5 — noi dung de AI trich dan.

CUM CAU HOI : how long does a thread lift last
              how many sessions do i need for melasma
              is thread lift safe
              thread lift vs filler which is better
VUNG        : Metro Manila
DICH VU     : Xline Thread Lift / Melasma

Yeu cau:
- Tra loi CAU HOI THAT, truoc, trong 2-3 cau. Khong vong vo, khong ban.
- Moi con so phai co nguon hoac ghi [CHO XAC NHAN].
- Neu ro gioi han: cai gi tuy co dia, cai gi can kham moi biet.
- Ghi ro dia diem (BGC/Taguig, Metro Manila) de AI gan dung ngu canh dia ly.
- Cuoi moi cau tra loi: mot dong nhan dang co so (ten - dia chi - hotline).
- KHONG cam ket ket qua, KHONG tuyen bo toi cao.

Tra ve theo tung trang dich, kem goi y tieu de H2/H3.
```

---

## Vì sao tập trung vào S3 và S4

AI được hỏi nhiều nhất đúng hai nhóm câu này — *"có an toàn không"* và *"mất bao lâu, bao nhiêu tiền"* — và đó cũng là hai nhóm **gần như không có nội dung tiếng Anh tốt cho thị trường Philippines**. Phần lớn kết quả hiện tại là nội dung Mỹ/Hàn, giá và bối cảnh không áp dụng được.

Đây là cùng một lợi thế với chặng S4 trong quảng cáo, chỉ khác kênh.

---

## Bốn luật viết nội dung cho AI trích dẫn

1. **Trả lời trước, giải thích sau.** AI trích đoạn đầu. Đoạn đầu mà là lời giới thiệu phòng khám thì không ai trích.
2. **Con số có đơn vị và có khoảng.** *"typically 12–18 months, depending on skin quality and technique"* trích được; *"long-lasting results"* không.
3. **Nêu giới hạn.** Nội dung nêu rõ *"this requires an in-person assessment"* được AI đánh giá đáng tin hơn nội dung khẳng định tuyệt đối.
4. **Gắn địa lý rõ ràng.** Ghi *"in Metro Manila"*, *"BGC, Taguig"* để AI gán đúng ngữ cảnh — người hỏi ở PH cần câu trả lời có giá và bối cảnh PH.

---

## Đo Share of Voice

Mỗi tháng hỏi lại 4 trợ lý AI đúng cụm câu hỏi trên, ghi lại:
- Có nhắc tên phòng khám không?
- Nếu có, nhắc ở vị trí nào trong câu trả lời?
- Thông tin được trích có **chính xác** không?

⚠️ Mục 3 quan trọng hơn mục 1. AI trích sai giá hoặc sai phạm vi dịch vụ là rủi ro, không phải thành tích.


===== prompt-nghien-cuu-tu-khoa.md =====

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


===== prompt-quy-trinh-tron-goi.md =====

# PROMPT — MODE 4 · CHẨN ĐOÁN & TỐI ƯU

> Tri thức: `kn-chan-doan-chi-so-ph.md` · `kn-quy-trinh-tuan-ph.md` · `kn-vung-philippines.md`.

---

## Khối lệnh

```
MODE 4 — chan doan.

KY SO LIEU : 01/10 - 21/10
DU LIEU    : [dan bang Ads + GA4 + CRM, CAT THEO VUNG V1-V4]

Chay dung 5 buoc:
 (1) So co tin duoc khong - tracking, trung lead, lead-Meta vs lead-CRM
 (2) GEO co dung Presence khong - KIEM TRUOC MOI THU
 (3) Phan ra chi phi/show-up - thanh phan nao xau di
 (4) Dinh vi tang ro dau tien, di tu tren xuong
 (5) Mua vu / bao / le / payday - KIEM CUOI

Tra ve:
 - Tang ro + chan doan xep theo xac suat
 - 3 viec lam tuan toi, xep theo THIET HAI NEU KHONG LAM
 - Ai so huu tung viec
 - So con thieu de ket luan chac hon
```

---

## ⚠️ Dữ liệu phải cắt theo vùng

Không có cột `vung` (V1–V4) thì **không chẩn đoán được gì** — và nguyên nhân số một của mọi triệu chứng trong gói này là geo.

Thiếu cột đó → agent phải nói thẳng *"thiếu tag `vung`, không kết luận được"*, ⛔ không đoán bừa.

---

## Ba triệu chứng đặc trưng và chẩn đoán đúng

| Triệu chứng | ⛔ Chẩn đoán sai hay gặp | ✅ Chẩn đoán đúng, theo thứ tự |
|---|---|---|
| **Lead nhiều, lịch hẹn ít** | *"Đội tư vấn kém"* | ① **Geo lọt V3/V4** ② truy vấn lệch ③ quảng cáo hứa khác trang nói |
| **CPL rẻ bất thường** | *"Chiến dịch chạy tốt"* | ① **Geo mở quá rộng** — gần như luôn là cái này |
| **Hẹn nhiều, không đến** | *"Khách không nghiêm túc"* | ① vùng xa, kẹt xe ② không nhắc lịch ③ **chưa biết giá, tới nơi mới biết** |

---

## Ngưỡng hành động

| Tín hiệu | Hành động |
|---|---|
| CPL ≥ 1,5× mục tiêu | Hạ bid 15% · rà search terms · ⛔ **chưa cắt** |
| ★ Chi phí/show-up ≥ 1,5× mục tiêu | ★ Đây mới là tín hiệu cắt. Kiểm geo trước |
| Chi ≥ 3× CPL, 0 lead | Tạm dừng từ khoá, rà trước khi xoá |
| Show-up < 50% | ⚠️ Vấn đề **vận hành**, không phải quảng cáo |
| Frequency > 3 / 7 ngày | Đổi creative, ⛔ đừng tăng ngân sách |

⛔ Không cắt chiến dịch dịch vụ giá trị ca cao chỉ vì CPL — độ trễ cân nhắc 2–6 tuần.

---

## Báo cáo tuần — bảy dòng

```
1. Chi · lead · booking · ĐẾN KHÁM        (so tuần trước, CÙNG LOẠI NGÀY)
2. Chi phí/show-up theo VÙNG V1–V4         ← dòng quan trọng nhất
3. Chi phí/show-up theo DỊCH VỤ
4. Chặng nào đang rò
5. Truy vấn lệch đã chặn tuần này
6. Ba việc tuần tới, xếp theo thiệt hại nếu không làm
7. [CHỜ XÁC NHẬN] nào còn thiếu
```

⛔ Không báo cáo bằng CPL ở dòng 1 mà không kèm số đến khám.


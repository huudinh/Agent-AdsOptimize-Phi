# TRI THỨC PHI — Ads Optimize Sunwoo Philippines
> File này gộp **9 module tri thức** từ `knowledge/`. Sinh tự động ngày 2026-10-23 bằng `python tools/gop-tham-khao.py`.
> ⛔ **Không sửa file này** — sửa ở bản rời trong thư mục nguồn rồi chạy lại lệnh trên.

**Cách đọc:** mỗi phần bắt đầu bằng dòng `===== tên file =====` và là **một đơn vị tri thức riêng**. Tham chiếu dạng `[[tên-file]]` trong văn bản trỏ tới **phần cùng tên ngay trong file này**, không phải file bên ngoài.

## MỤC LỤC

| # | File | Cỡ |
|---|---|---|
| 1 | `kn-chan-doan-chi-so-ph.md` | 7.3 KB |
| 2 | `kn-chan-dung-hanh-trinh-ph.md` | 9.9 KB |
| 3 | `kn-cong-win-tu-khoa-ph.md` | 6.8 KB |
| 4 | `kn-engine-win-ad-ph.md` | 6.6 KB |
| 5 | `kn-ho-so-thuong-hieu-sunwoo.md` | 10.7 KB |
| 6 | `kn-khung-landing-ph.md` | 6.3 KB |
| 7 | `kn-quy-trinh-tuan-ph.md` | 4.9 KB |
| 8 | `kn-rao-phap-ly-ph.md` | 10.9 KB |
| 9 | `kn-vung-philippines.md` | 10.3 KB |


===== kn-chan-doan-chi-so-ph.md =====

# CHẨN ĐOÁN CHỈ SỐ — PHỄU 7 TẦNG
Version 1.0 · Cập nhật 2026-10-23

---

## 1 · ⚠️ Đo bằng chi phí/khách ĐẾN KHÁM, không bằng CPL

**CPL là chỉ số gây hiểu lầm nhất của gói này**, vì hai lý do cộng lại:

1. **Geo.** Mở rộng ra cả nước làm CPL rẻ đi ngay lập tức — và không ai trong số lead mới đến khám được.
2. **Rào BỀN.** Quảng cáo nêu tổng chi phí sẽ **làm CPL xấu đi** nhưng làm tỷ lệ đến khám tốt lên. Đo bằng CPL là kết luận ngược.

> **Chỉ số trục của gói này: `chi phí / khách ĐẾN KHÁM` (cost per show-up).**
> CPL chỉ là chỉ số **phụ trợ để chẩn đoán**, ⛔ không phải chỉ số để quyết định.

---

## 2 · Phễu 7 tầng — định nghĩa bằng công thức

| # | Tầng | Chỉ số | Công thức | Nguồn |
|---|---|---|---|---|
| ① | Chi phí | **Spend** | tổng chi | Ads |
| ② | Hiển thị | **CPM** · **Frequency** | chi÷impr×1000 · impr÷reach | Ads |
| ③ | Click | **CTR** · **CPC** | click÷impr · chi÷click | Ads |
| ④ | Trang | **Tỷ lệ cuộn ≥ 75%** · thời gian trên trang | — | GA4 |
| ⑤ | Lead | **CPL** · tỷ lệ click→lead | chi÷lead hợp lệ | Ads + CRM |
| ⑥ | **Lịch hẹn** | **CPB** · lead→booking | chi÷booking | CRM |
| ⑦ | ★ **Đến khám** | ★ **Chi phí/show-up** · booking→show | **chi÷lượt đến** | CRM |
| ⑧ | Chốt | **CAC** · show→chốt · **ROAS** | chi÷ca chốt | CRM/ERP |

🔴 **Bốn định nghĩa phải chốt bằng văn bản một lần, trước khi chạy:**
1. **"Lead hợp lệ"** = có số điện thoại dùng được **+** dịch vụ quan tâm **+ đã qua lọc rác**. ⚠️ Lead-Meta ≠ lead-CRM, chênh 15–30% là bình thường.
2. **"Lead rác"** = danh sách lý do đóng được, ⛔ không để *"cảm thấy rác"*: số sai sau 3 lần gọi · ngoài vùng V4 · ⛔ không có nhu cầu · trùng trong 30 ngày · ứng viên xin việc · hỏi dịch vụ ngoài phạm vi.
3. **"Booking"** = lịch có **ngày–giờ cụ thể** và khách **đã xác nhận**.
4. **"Đến khám"** = đã có mặt tại phòng khám, ghi nhận trong CRM.

⛔ Không có bốn định nghĩa này thì mọi báo cáo phía sau đều vô nghĩa.

---

## 3 · Ba tag CRM bắt buộc — gắn từ ngày đầu

| Tag | Giá trị | Không có thì mất gì |
|---|---|---|
| `vung` | V1 / V2 / V3 / V4 | ⛔ **Không chẩn đoán được geo** — nguyên nhân số 1 của *"lead nhiều, không ai đến"* |
| `dich_vu` | 1 trong 6 | Không biết dịch vụ nào đáng đổ tiền |
| `chang` | S2 / S3 / S4 / S5 | Không biết chặng nào đang rò |

⛔ **Không gắn đủ 3 tag từ ngày đầu thì Pha 2 không làm được.** Đây là việc 30 phút ở tuần 1, hoặc là việc không bao giờ làm được nữa.

---

## 4 · Bảng triệu chứng → tầng rò → ai xử lý

| Triệu chứng | Tầng rò | Chẩn đoán (xếp theo xác suất) | Ai xử lý |
|---|---|---|---|
| ★ **Lead nhiều, lịch hẹn ít** | ⑤→⑥ | ① **Geo sai — lead V3/V4 lọt vào** ② truy vấn lệch ③ quảng cáo hứa một đằng trang nói một nẻo | **Ads** |
| ★ **Lịch hẹn nhiều, không đến** | ⑥→⑦ | ① **Vùng xa, kẹt xe** ② không nhắc lịch ③ hẹn quá xa ngày ④ **chưa biết giá, tới nơi mới biết** | **CSKH + Ads** |
| CPL rẻ bất thường | ⑤ | ⚠️ **Gần như luôn là geo mở quá rộng.** Kiểm `geo_mode` **trước tiên** | Ads |
| CTR cao, lead ít | ③→⑤ | ① trang đích sai chặng ② form đặt quá sớm ③ trang tải chậm trên 4G | Ads + Kỹ thuật |
| Inbox nhiều, không cho số | ⑤ | ① chậm phản hồi lần đầu ② không có ca trực tối/cuối tuần ③ xin số quá sớm | **Trực page** |
| CPM tăng, CPL giữ | ② | **Không có vấn đề gì.** Chỉ ghi nhận | — |
| Chi hụt ngân sách | ① | ① tệp quá hẹp ② bid trần thấp ③ **creative vừa bị từ chối** → kiểm policy trước | Ads |
| Tuần này tệ hơn tuần trước | — | ⚠️ Kiểm **bão · lễ · payday** trước khi kết luận xu hướng | — |

**Quy trình chẩn đoán 5 bước, không bỏ bước:**
```
① Số có tin được không?  (tracking · trùng lead · lead-Meta vs lead-CRM)
② Geo có đúng không?     ★ kiểm Presence TRƯỚC MỌI THỨ KHÁC
③ Phân rã chi phí/show-up → thành phần nào xấu đi
④ Định vị tầng rò đầu tiên, đi từ trên xuống
⑤ Mùa vụ · bão · lễ · payday — kiểm CUỐI, không kiểm đầu
```

⚠️ **Bước ⑤ đứng cuối là có chủ ý.** Kiểm mùa vụ trước sẽ lấy *"tại mùa"* ra giải thích mọi thứ và không ai phải sửa gì.

---

## 5 · Ngưỡng hành động

| Quy tắc | Hệ số | Hành động |
|---|---|---|
| CPL vượt ngưỡng | ≥ 1,5× mục tiêu | Hạ bid 15% · rà search terms · ⛔ **chưa cắt** |
| Chi phí/show-up vượt | ≥ 1,5× mục tiêu | ★ Đây mới là tín hiệu cắt. Rà geo và trang đích |
| 0 lead | chi ≥ 3× CPL mục tiêu | Tạm dừng từ khoá, rà trước khi xoá |
| Tỷ lệ show-up < 50% | — | ⚠️ Vấn đề vận hành, ⛔ không phải vấn đề quảng cáo. Rà nhắc lịch + minh bạch giá |
| Frequency > 3 (Meta, 7 ngày) | — | Đổi creative, ⛔ đừng tăng ngân sách |

⛔ **Không cắt chiến dịch dịch vụ giá trị ca cao chỉ vì CPL.** Thread Lift và liệu trình Melasma có độ trễ cân nhắc **2–6 tuần** — cắt ở tuần 3 là cắt trước khi dữ liệu về.

---

## 6 · Lộ trình ba pha

| Pha | Thời gian | Chiến lược | Điều kiện sang pha sau |
|---|---|---|---|
| **1 · Học** | Tuần 1–6 | Manual CPC · Phrase · phủ định dày · chạy V1+V2 | Đủ 3 tag CRM · ≥ 30 lead có `vung` · đã biết chi phí/show-up theo vùng |
| **2 · Chuẩn** | Tuần 7–14 | Chuyển Max conversions theo **booking**, ⛔ không theo lead · mở V3 cho dịch vụ giá trị cao | Chi phí/show-up ổn định 4 tuần liền |
| **3 · Mở rộng** | Tuần 15+ | Mở nhóm **N1 Hàn Quốc** nếu có nhân sự · test V4 nếu CRM chứng minh có ca thật | — |

⛔ **Không đặt mục tiêu tối ưu theo "Lead" ở Pha 2.** Tối ưu theo lead là dạy máy đi tìm thêm lead V4 — thứ rẻ nhất và vô dụng nhất.

---

## 7 · Báo cáo tuần — bảy dòng, không hơn

```
1. Chi · lead · booking · ĐẾN KHÁM        (4 số, kèm % so tuần trước cùng loại ngày)
2. Chi phí/show-up theo VÙNG V1–V4        ← dòng quan trọng nhất
3. Chi phí/show-up theo DỊCH VỤ (6 mục)
4. Chặng nào đang rò                       (theo bảng §4)
5. Truy vấn lệch đã chặn tuần này
6. Ba việc làm tuần tới, xếp theo thiệt hại nếu không làm
7. Số đang chờ: [CHỜ XÁC NHẬN] nào còn thiếu
```

⛔ **Không báo cáo bằng CPL ở dòng 1** mà không kèm số đến khám — đó là cách một đội tự khen nhau trong sáu tuần rồi mới phát hiện không ai tới phòng khám.


===== kn-chan-dung-hanh-trinh-ph.md =====

# CHÂN DUNG KHÁCH HÀNG & HÀNH TRÌNH S1–S6
Version 1.0 · Cập nhật 2026-10-23

---

## 1 · Luật nền: chọn NGƯỜI trước, chọn từ khoá sau

Trật tự bắt buộc, đảo là quay về cách làm cũ:

```
vùng (V1–V4) → chân dung → chặng S1–S6 → chiến dịch → landing → từ khoá → phủ định → ngưỡng
```

**Tách hẳn hai cặp đối lập**, vì mỗi cặp cần bằng chứng khác nhau:
- **Khách lần đầu** vs **khách đã làm ở nơi khác và không hài lòng** — nhóm sau đã mất niềm tin vào cả ngành, trả được CPC cao nhất, và cần bằng chứng về **bác sĩ**, không phải về **máy**.
- **Người gõ tìm kiếm** vs **người điều trị** — mẹ tìm cho con tuổi teen bị mụn, chồng tìm cho vợ, con tìm cho mẹ. Thông điệp phải nói với **người gõ**, bằng chứng phải thuyết phục **người điều trị**.

---

## 2 · ⚠️ BỐN RÀO CẢN — rào thứ tư là **BỀN**

Gói nội địa Việt Nam có **SỢ · NGỜ · NGẠI**. Gói quốc tế thêm **XA**.
Gói này — thủ thuật không phẫu thuật, nhiều buổi, có thời hạn — thêm **BỀN**.

| Rào | Khách nghĩ | Gỡ bằng |
|---|---|---|
| **SỢ** | *"Có đau không? Có bị hỏng mặt không? Chỉ nâng nó có lòi ra không?"* | Mô tả cảm giác thật từng bước · tên thuốc tê · ai xử lý nếu có phản ứng · số buổi theo dõi |
| **NGỜ** | *"Chỗ này có bác sĩ thật không hay chỉ là spa? Máy có chính hãng không?"* | ★ **Diplomate PDS** · PRC license · tên thiết bị cụ thể · chứng nhận FDA PH của thiết bị |
| **NGẠI** | *"Bao nhiêu tiền? Nghỉ mấy ngày? Có ai biết tôi đi làm không?"* | Giá công khai · downtime bằng giờ/ngày · phòng riêng · lịch ngoài giờ |
| ★ **BỀN** | *"Được bao lâu rồi lại phải làm tiếp? Tôi phải trả tiền này mãi à?"* | **Số buổi liệu trình · tổng chi phí · hiệu quả kéo dài bao lâu · chi phí duy trì/năm** |

### Vì sao BỀN là rào quyết định của gói này

Ba rào đầu là rào **trước khi làm**. BỀN là rào **sau khi đã muốn làm** — khách đã tin bác sĩ, đã chấp nhận giá một buổi, rồi mới nghĩ tới câu *"vậy năm sau thì sao"*. Mất khách ở đây là đắt nhất vì họ đã đi gần hết phễu.

Và đây là rào mà **gần như cả ngành né tránh**: ai cũng quảng cáo *"starts at ₱X"* cho một buổi, không ai nói tổng. Khách biết điều đó, nên họ mặc định **không tin con số trong quảng cáo**.

> **Phép thử trước khi xuất bất kỳ landing hay mẫu quảng cáo nào:**
> *"Đọc xong, khách có tính được mình sẽ tốn bao nhiêu trong 12 tháng tới không?"*
> Chưa → chưa xong.

**Bốn câu của rào BỀN, theo đúng thứ tự khách nghĩ:**

| # | Khách nghĩ | Trang phải trả lời bằng |
|---|---|---|
| 1 | *"Cần mấy buổi mới thấy kết quả?"* | **Một con số khoảng** + mốc nào thì thấy |
| 2 | *"Tổng cộng hết bao nhiêu?"* | Giá trọn gói, ⛔ không chỉ giá một buổi |
| 3 | *"Giữ được bao lâu?"* | Khoảng thời gian thật, kèm *"tuỳ cơ địa"* |
| 4 | *"Sau đó phải làm gì để giữ?"* | Nhịp duy trì + chi phí duy trì |

⛔ Không có bốn con số này thì **không chạy MODE 2 và MODE 3** — xem `[CHỜ XÁC NHẬN]` mục 1–2 ở hồ sơ thương hiệu.

---

## 3 · PHỄU 6 CHẶNG — chặng quyết định là **S4**

| Chặng | Dấu hiệu từ khoá | Rào | Landing | Chạy ads? |
|---|---|---|---|---|
| **S1 NHẬN BIẾT** | `what is thread lift` · `why am i losing hair` | — | — | ❌ Không chạy Search chốt. Nuôi bằng content/TikTok |
| **S2 SO SÁNH CÁCH LÀM** | `thread lift vs filler` · `picosure vs laser` · `is thread lift worth it` | NGỜ | **L1 So sánh** | ✅ Bid thấp, nuôi phễu. ⛔ Không bán Sunwoo ở trang này |
| **S3 NỖI SỢ & AN TOÀN** | `thread lift side effects` · `does it hurt` · `gone wrong` · `review` | **SỢ** | **L2 Trả lời thẳng** | ✅ Gọi tên nỗi lo rồi trả lời ngay |
| **S4 SỐ BUỔI & TỔNG CHI PHÍ ★★** | `how many sessions` · `how long does it last` · `total cost` · `maintenance` · `package price` | **BỀN** | **L3 Liệu trình & chi phí** | ✅ ★ **Chặng quyết định** |
| **S5 CHỌN NƠI LÀM** | `thread lift bgc` · `dermatologist taguig` · `best clinic near me` · `book` | NGẠI | **L4 Đặt lịch** | ✅ Bid cao nhất |
| **S6 SAU ĐIỀU TRỊ & QUAY LẠI** | `aftercare` · `swelling after` · `touch up` | BỀN | Trang CRM | ❌ Không chạy ads. Trang cho CRM/Messenger |

### Vì sao S4 là chặng của gói này

Khách đến S4 **đã vượt qua cả SỢ và NGỜ** — họ muốn làm, chỉ đang tính xem có kham nổi lâu dài không.

- Từ khoá S4 có **cạnh tranh thấp nhất trong cả phễu**: đối thủ đổ tiền vào `thread lift price` và `best clinic`, gần như không ai làm trang trả lời *"how many sessions"* và *"how long does it last"*.
- Người gõ S4 có **ý định mua cao hơn** người gõ S2 nhưng **giá thầu rẻ hơn** người gõ S5.
- Và nó là chặng khách **nhớ nhất**, vì đó là câu không ai trả lời cho họ.

→ **Ngân sách tối thiểu: S4 ≥ 20% · S3 ≥ 15% · S5 ≥ 30%.** Chia theo **ý định mua × giá trị ca**, ⛔ không theo lượng tìm kiếm.

---

## 4 · Sáu chân dung gốc — khuôn để viết `chan_dung[]`

Mỗi bộ market JSON cần **4–7 chân dung**. Sáu chân dung dưới đây là khuôn, phải chỉnh theo dịch vụ.

| Mã | Ai | Insight (lời khách) | Rào nặng nhất | Vào ở | Giá trị ca |
|---|---|---|---|---|---|
| **CD1** | Nữ 32–45, BGC/Makati, văn phòng, bắt đầu thấy chảy xệ | *"Tôi chưa muốn phẫu thuật. Tôi chỉ muốn nhìn đỡ mệt mỏi hơn, mà thứ hai vẫn đi làm được."* | **BỀN** + NGẠI (downtime) | S2–S4 | **Cao** (Thread Lift) |
| **CD2** | Nữ 28–40, Metro Manila, nám sau sinh | *"Tôi thử hết kem rồi. Tôi không muốn thử nữa, tôi muốn biết cái này có hết hẳn không hay lại lên lại."* | **BỀN** — nám tái phát | S3–S4 | Trung bình–Cao (liệu trình) |
| **CD3** | Nam 28–42, BGC, rụng tóc hói trán | *"Tôi không muốn ai biết tôi đi làm cái này."* | **NGẠI** (riêng tư) + NGỜ | S2–S4 | Cao (Meso Hair nhiều buổi) |
| **CD4** | Nữ/Nam 18–26, sinh viên hoặc đi làm, mụn viêm | *"Tôi đã đi 3 chỗ rồi, đỡ rồi lại lên."* **Người gõ có thể là mẹ.** | **NGỜ** — mất niềm tin vào ngành | S3 | Thấp–Trung bình |
| **CD5** | Khách **đã làm ở nơi khác, không hài lòng** | *"Tôi làm chỗ kia, không thấy gì. Lần này tôi muốn biết ai là người cầm máy."* | **NGỜ** nặng nhất | S3–S5 | **Cao** — trả được CPC cao nhất |
| **CD6** | Người Hàn sống tại McKinley Hill | *"Ở Seoul tôi làm chỗ quen. Ở đây có chỗ nào làm đúng chuẩn đó không?"* | NGỜ — tiêu chuẩn | S5 | Cao |

**Hai điều bắt buộc khi viết `insight`:**
1. Viết bằng **lời khách**, không viết bằng lời marketing. *"Khách quan tâm đến giải pháp trẻ hoá"* là một câu rỗng.
2. Ghi rõ **người gõ có phải người điều trị không**, và **vành đai V1–V4**. Thiếu hai thứ này thì không chọn được landing lẫn geo.

---

## 5 · Bốn quy tắc viết thông điệp theo rào cản

**① Gọi tên rào, đừng gọi tên dịch vụ.**
⛔ *"Xline Thread Lift tại Sunwoo"* — nói về mình.
✅ *"Chảy xệ nhẹ nhưng chưa muốn phẫu thuật?"* — nói về khách. Tên dịch vụ để ở dòng sau.

**② Một trang gỡ MỘT rào.**
Trang gỡ cả bốn rào là trang không gỡ rào nào. S3 gỡ SỢ, S4 gỡ BỀN — ⛔ không trộn.

**③ Bằng chứng phải khớp rào.**
| Rào | Bằng chứng đúng | ⛔ Bằng chứng sai |
|---|---|---|
| SỢ | Mô tả cảm giác từng bước, tên thuốc tê, quy trình xử lý phản ứng | Ảnh kết quả đẹp |
| NGỜ | Diplomate PDS, PRC, tên máy, số năm | Lời chứng thực chung chung |
| NGẠI | Con số giá, con số downtime, lịch ngoài giờ | *"Giá cả phải chăng"* |
| **BỀN** | **Số buổi · tổng gói · thời gian giữ · chi phí duy trì** | *"Hiệu quả lâu dài"* |

**④ ⛔ Không chê ngoại hình khách.** Vừa là rào đạo đức, vừa là **vi phạm chính sách nền tảng** — xem `kn-rao-phap-ly-ph.md` §5. *"Are you struggling with acne?"* bị chặn; *"Acne treatment options from board-certified dermatologists"* thì không.

---

## 6 · Micro-conversion — thứ phải có trước form

Khách PH ngại để lại số điện thoại cho một phòng khám chưa biết. Đặt **một bước nhỏ hơn** trước form:

| Micro | Dùng cho chặng | Vì sao hiệu quả |
|---|---|---|
| **Tải bảng liệu trình & chi phí (PDF)** | ★ S4 | Đúng thứ khách đang thiếu. Đổi được email/số mà không phải cam kết gì |
| **Bộ câu hỏi nên hỏi bác sĩ trước khi làm** | S3 | Gỡ rào SỢ, đồng thời định khung tiêu chí theo thế mạnh của phòng khám |
| **Chat Messenger hỏi giá** | S5 | Rào thấp nhất ở PH. ⚠️ Phải có người trực, ⛔ không auto-reply rồi im |
| **Đặt lịch tư vấn miễn phí** | S5 | CTA chính. Miễn phí đã là micro rồi |

⛔ **Không đặt form 6 trường ở đầu trang.** Giữ đúng 4 trường của form hiện tại (tên · số · dịch vụ · khu vực) và đặt **sau** phần trả lời rào cản.


===== kn-cong-win-tu-khoa-ph.md =====

# CỔNG WIN TỪ KHOÁ — 4 TIÊU CHÍ, QUA 3/4 MỚI ĐƯỢC CHẠY
Version 1.0 · Cập nhật 2026-10-23

---

## 1 · Bốn tiêu chí

Mỗi từ khoá chấm **4 tiêu chí, mỗi tiêu chí 1 điểm**. **≥ 3/4 mới được bật.** Ghi điểm vào cột `win` dạng `3/4`.

| # | Tiêu chí | Đạt khi |
|---|---|---|
| ① | **Ý định mua** | Người gõ đang muốn **làm**, không phải đang muốn **đọc**. `thread lift price bgc` đạt; `what is thread lift` không |
| ② | **Phục vụ được** | Dịch vụ nằm trong **6 dịch vụ** của phòng khám và trong **phạm vi giấy phép** |
| ③ | **Đến được** | Người gõ ở **V1/V2**, hoặc V3 với dịch vụ giá trị ca cao. ⛔ V4 không đạt |
| ④ | **Trang sẵn sàng** | Đã có landing đúng **chặng** và đúng **rào cản** của từ khoá đó |

**Ví dụ chấm:**

| Từ khoá | ① | ② | ③ | ④ | WIN | Quyết |
|---|---|---|---|---|---|---|
| `thread lift bgc price` | ✅ | ✅ | ✅ | ✅ | **4/4** | Bật, bid cao |
| `how many sessions for melasma` | ✅ | ✅ | ✅ | ❌ chưa có L3 | **3/4** | Bật **sau khi** dựng L3 |
| `best dermatologist philippines` | ✅ | ✅ | ❌ cả nước | ✅ | **3/4** | ⚠️ Bật **kèm Presence + giới hạn vùng** |
| `thread lift cebu` | ✅ | ✅ | ❌ | ❌ | **2/4** | ⛔ Loại + thêm `cebu` vào phủ định |
| `is thread lift painful` | ❌ đọc | ✅ | ✅ | ✅ | **3/4** | Bật ở S3, bid thấp, mục tiêu micro |

⛔ **Không bật từ khoá 2/4** dù lượng tìm kiếm lớn. Lượng tìm kiếm không phải tiêu chí — nó không nằm trong bốn ô trên, và đó là có chủ ý.

---

## 2 · ⚠️ Cổng GEO — tiêu chí ③ có luật riêng

**Mọi dòng từ khoá phải khai hai trường:**

| Trường | Nghĩa | ⛔ Nhầm hay gặp |
|---|---|---|
| `market` | Người gõ **đang ở đâu** (V1/V2/V3/V4) | Nhầm với thành phố **trong chuỗi từ khoá** |
| `geo_mode` | Luôn là **`Presence`** | Để Google tự chọn |

> `dermatologist taguig` gõ từ **Makati** = V2, sắp đặt lịch → cần giá và lịch trống.
> `dermatologist taguig` gõ từ **Cebu** = V4, đang tìm hiểu từ xa → ⛔ không phải khách của phòng khám này.
> **Cùng chuỗi ký tự, hai người khác nhau.** Chỉ `Presence` mới tách được.

---

## 3 · Sáu nhóm từ khoá theo chặng

Tên nhóm quảng cáo đặt theo khuôn — **khoá nối sang sheet 2 và sheet 5 của file Excel**:

```
PHI | <vùng> | <dịch vụ> | <chặng> | <cụm truy vấn>

PHI | V1 | ThreadLift | S4 | Sessions & Total Cost
PHI | V2 | Melasma | S3 | Safety & Side Effects
PHI | V1 | MesoHair | S5 | Book BGC
```

| Chặng | Cụm truy vấn | Dấu hiệu | Bid |
|---|---|---|---|
| S2 | So sánh cách làm | `vs` · `which is better` · `worth it` | Thấp |
| S3 | An toàn & nỗi sợ | `side effects` · `painful` · `safe` · `gone wrong` · `review` | Trung bình |
| **S4 ★** | **Số buổi & chi phí** | `how many sessions` · `how long does it last` · `total cost` · `package` · `maintenance` | **Trung bình — ưu tiên ngân sách** |
| S5 | Chọn nơi làm | `near me` · `bgc` · `taguig` · `makati` · `book` · `clinic` | **Cao nhất** |

⛔ **Không gộp S3 và S5 vào một nhóm quảng cáo.** Người hỏi *"có đau không"* và người gõ *"book thread lift bgc"* cần hai mẫu quảng cáo và hai trang khác nhau. Gộp là cách giết cả hai.

---

## 4 · Phủ định — ba lớp

### Lớp 1 · Phủ định toàn tài khoản
| Nhóm | Từ | Khớp | Lý do |
|---|---|---|---|
| **Ngoài vùng** | `cebu` · `davao` · `baguio` · `iloilo` · `bacolod` · `clark` | Phrase | V4, không đến được |
| **Miễn phí / học** | `free` · `diy` · `home remedy` · `natural way` · `tutorial` | Phrase | Không mua dịch vụ. ⚠️ **Miễn trừ** cho `free consultation` |
| **Việc làm** | `job` · `hiring` · `salary` · `training` · `course` · `certification` | Phrase | Ứng viên, không phải khách |
| **Ngoài phạm vi** | `surgery` · `rhinoplasty` · `liposuction` · `dental` · `braces` | Phrase | ⛔ Ngoài 6 dịch vụ. Xem lỗi ② hồ sơ thương hiệu |
| **Sản phẩm** | `cream` · `serum` · `shampoo` · `supplement` · `pills` | Phrase | Tìm mua sản phẩm, không tìm thủ thuật |
| **Giá rẻ cực đoan** | `cheapest` · `under 1000` · `promo only` | Phrase | Không khớp định vị |

### Lớp 2 · Phủ định chéo giữa các chặng
| Nhóm | Từ | Áp vào | Lý do |
|---|---|---|---|
| S2 không lấy truy vấn giá | `price` · `cost` · `how much` | nhóm S2 | Truy vấn giá thuộc S4/S5 và cần trang khác |
| S5 không lấy truy vấn học | `what is` · `vs` | nhóm S5 | Đổ người đang đọc vào trang đặt lịch là lãng phí bid cao |
| S4 không lấy truy vấn nơi làm | `near me` · `clinic` | nhóm S4 | Thuộc S5 |

### Lớp 3 · Phủ định theo dịch vụ
Chặn chéo giữa 6 dịch vụ: nhóm `Melasma` phủ định `acne`, `hair`, `thread`; nhóm `MesoHair` phủ định `transplant` *(ngoài phạm vi)*…

**Nhịp rà:** search terms **2 lần/tuần** ở Pha 1, **1 lần/tuần** từ Pha 2.
⛔ Thêm phủ định mà không ghi lý do vào file JSON → ba tháng sau không ai biết vì sao chặn, và sẽ có người mở lại.

---

## 5 · Quy tắc khớp

| Chặng | Khớp dùng | Lý do |
|---|---|---|
| S2 · S3 | **Phrase** | Cần độ phủ để học truy vấn thật, nhưng không thả rông |
| **S4** | **Phrase** + Exact cho cụm đã chứng minh | Cụm S4 dài và đa dạng, Exact một mình thì bỏ sót |
| S5 | **Exact** cho cụm chốt + Phrase cho biến thể vùng | Bid cao nhất, phải kiểm soát chặt |

⛔ **Không dùng Broad ở Pha 1.** Chưa có danh sách phủ định đủ dày thì Broad đốt ngân sách vào truy vấn ngoài vùng và ngoài phạm vi giấy phép — và lỗi thứ hai là lỗi pháp lý, không chỉ là lỗi tiền.

---

## 6 · Ngưỡng dừng một từ khoá

| Dấu hiệu | Ngưỡng | Hành động |
|---|---|---|
| Chi nhiều, không lead | Chi ≥ **3× CPL mục tiêu**, 0 lead | Tạm dừng, rà search terms trước khi xoá |
| CPL vượt ngưỡng | ≥ **1,5× CPL mục tiêu**, đủ mẫu | Hạ bid 15%, kiểm trang đích |
| Lead về nhưng không đến khám | ≥ 5 lead, 0 lịch hẹn | ⚠️ Kiểm `market` — gần như luôn là **lead V4 lọt vào** |
| Truy vấn lệch > 30% | — | Thêm phủ định, ⛔ đừng vội đổi từ khoá |

⚠️ **"Lead về nhưng không đến khám" là triệu chứng đặc trưng của gói này.** Nguyên nhân số một không phải chất lượng tư vấn — là **geo**. Kiểm cổng GEO trước khi đổ lỗi cho đội trực.


===== kn-engine-win-ad-ph.md =====

# ENGINE WIN-AD — SINH MẪU QUẢNG CÁO
Version 1.0 · Cập nhật 2026-10-23

---

## 1 · Bảy bước B1→B7, không bỏ bước

```
B1 Chốt chặng + rào cản      →  B2 Chốt chân dung + vùng V1–V4
B3 Lấy bằng chứng khớp rào   →  B4 Sinh 15 headline + 4 description
B5 Chấm bảng 14 điểm         →  B6 Rà 12 ô pháp lý
B7 Xuất + danh sách claim cần pháp chế duyệt
```

⛔ Bỏ B1 → ra mẫu quảng cáo nói chung chung cho mọi người. Bỏ B5 → không biết mẫu nào đáng chạy. Bỏ B6 → mẫu bị chặn hoặc tệ hơn, được duyệt rồi mới thành vấn đề giấy phép.

---

## 2 · Google Search — 15 headline · 4 description

**Ràng buộc kỹ thuật:** headline ≤ **30 ký tự** · description ≤ **90 ký tự**.

**Phân bổ 15 headline theo vai trò** — ⛔ không viết 15 biến thể của cùng một câu:

| Vai trò | Số lượng | Ví dụ (S4 · Thread Lift) |
|---|---|---|
| Gọi tên rào cản | 3 | `How Long Does It Last?` · `Sessions & Total Cost` |
| Bằng chứng chuyên môn | 3 | `Board-Certified Dermatologist` · `PDS Diplomate On Site` |
| Vùng / địa điểm | 3 | `Thread Lift in BGC` · `McKinley Hill, Taguig` |
| Lợi ích cụ thể | 3 | `Lunch-Hour Visit` · `Back To Work Same Day` |
| CTA | 3 | `Free Consultation` · `Book A Slot Today` |

**4 description, mỗi cái một việc:**
1. Trả lời rào cản chính bằng **một con số**.
2. Bằng chứng chuyên môn + địa điểm.
3. Điều khách còn băn khoăn tiếp theo.
4. CTA + miễn trừ ngắn.

⛔ **Pin headline chỉ khi bắt buộc.** Pin cứng cả 3 vị trí là tự tắt khả năng học của Google.

---

## 3 · Meta — 3–5 biến thể

| Khối | Luật |
|---|---|
| **Primary text** | ★ **Taglish**. 2–3 câu. Câu đầu phải là câu khách tự nói trong đầu |
| **Headline** | English chuẩn, ≤ 40 ký tự. Tên dịch vụ + vùng |
| **Description** | Bằng chứng chuyên môn |
| **Creative** | ⛔ Không cận cảnh khuyết điểm. Chân dung bình thường, hoặc cảnh phòng khám, hoặc bác sĩ |
| **CTA** | `Learn More` cho S3/S4 · `Book Now` cho S5 |

**Ví dụ đạt (S4 · Meso Hair · CD3 nam BGC):**
```
Primary : Ilang sessions ba talaga bago may makita? Sabihin na namin nang diretso —
          at kung magkano lahat-lahat. Walang hidden package.
Headline: Meso Hair Therapy in BGC
Desc    : Assessed by a board-certified dermatologist.
CTA     : Learn More  →  LP3 (liệu trình & chi phí)
```

**Ví dụ KHÔNG đạt:**
```
⛔ "Nahihiya ka ba sa buhok mo?"   → chê ngoại hình người xem, Meta chặn
⛔ "Guaranteed hair regrowth!"      → cam kết kết quả, trượt ô ② pháp lý
⛔ "The #1 hair clinic in PH"       → tuyên bố tối cao, trượt ô ③
```

---

## 4 · ⚠️ BẢNG CHẤM 14 ĐIỂM — dưới 10 không chạy

| # | Tiêu chí | Điểm | 0 điểm khi |
|---|---|---|---|
| ① | Nói về **khách**, không nói về mình | 1 | Mở đầu bằng tên phòng khám |
| ② | Gọi đúng **một** rào cản | 1 | Gỡ chung chung cả bốn |
| ③ | Có **con số cụ thể** | 1 | Toàn tính từ |
| ④ | Bằng chứng **khớp** rào cản | 1 | Rào NGỜ mà đưa ảnh đẹp |
| ⑤ | Đúng **chặng** của từ khoá | 1 | Mẫu chốt gắn vào từ khoá S2 |
| ⑥ | Trang đích **đúng chặng** | 1 | S4 đổ về trang đặt lịch |
| ⑦ | ★ **`geo_mode = Presence`** | 1 | **0 điểm → LOẠI THẲNG**, không tính tổng |
| ⑧ | Có **vùng** trong mẫu (BGC/Taguig…) | 1 | Không nêu địa điểm |
| ⑨ | Đúng ngôn ngữ theo kênh | 1 | Taglish trên Google Search |
| ⑩ | Qua **12 ô pháp lý** | 1 | **0 điểm → LOẠI THẲNG** |
| ⑪ | Không chê ngoại hình | 1 | Câu *"Are you struggling with…"* |
| ⑫ | CTA khớp chặng | 1 | `Book Now` ở S2 |
| ⑬ | Có **micro-conversion** cho S3/S4 | 1 | Chỉ có form đặt lịch |
| ⑭ | ★ Trả lời được rào **BỀN** *(bắt buộc với S4)* | 1 | Không nêu số buổi / tổng chi phí |

**Luật đọc điểm:**
- **⑦ hoặc ⑩ = 0 → LOẠI THẲNG.** Không bù, không tính tổng.
- **< 10/14** → viết lại, không chạy.
- **10–11** → chạy được, ghi rõ tiêu chí thiếu để vòng sau sửa.
- **≥ 12** → ưu tiên ngân sách.

---

## 5 · Mười công thức headline dùng được

| # | Công thức | Chặng | Ví dụ |
|---|---|---|---|
| 1 | *Câu hỏi khách tự hỏi* | S3 · S4 | `How Long Does It Last?` |
| 2 | *Con số + đơn vị* | S4 | `4 Sessions, One Price` |
| 3 | *Dịch vụ + vùng* | S5 | `Thread Lift in BGC` |
| 4 | *Bằng chứng chuyên môn* | S3 | `PDS Diplomate Dermatologist` |
| 5 | *Downtime* | S3 · S5 | `Back To Work Same Day` |
| 6 | *So sánh trung lập* | S2 | `Thread Lift Or Filler?` |
| 7 | *Gỡ rào riêng tư* | S3 | `Private Suite Consultation` |
| 8 | *CTA miễn phí* | S5 | `Free Doctor Consultation` |
| 9 | *Chống mập mờ giá* | ★ S4 | `No Hidden Package Fees` |
| 10 | *Chuẩn Hàn* | S2 · S5 | `Korean-Standard Protocol` |

⛔ **Không dùng:** `Best in PH` · `Guaranteed Results` · `Transform Your Life` · `Limited Slots` *(nếu không thật)*.

---

## 6 · Luật sinh theo chặng

| Chặng | Mẫu phải có | Mẫu ⛔ không được có |
|---|---|---|
| **S2** | So sánh **trung lập** hai cách làm, tiêu chí chọn | Bán Sunwoo · giá · `Book Now` |
| **S3** | Gọi tên nỗi sợ + trả lời **ngay trong mẫu** | Ảnh kết quả đẹp thay cho câu trả lời |
| **S4 ★** | **Số buổi · tổng chi phí · thời gian giữ** | Chỉ nêu giá một buổi |
| **S5** | Vùng · lịch trống · CTA đặt lịch | Giải thích dịch vụ từ đầu |

---

## 7 · Nhịp A/B — bốn phép thử đáng chạy trước

| Test | A | B | Đo bằng | Thời gian |
|---|---|---|---|---|
| **T1 ★** | Nêu **tổng chi phí liệu trình** | Chỉ nêu *"starts at ₱X"* | Tỷ lệ lead → **đến khám** | 6 tuần |
| T2 | Headline nêu **bằng cấp bác sĩ** | Headline nêu **tên máy** | CTR + tỷ lệ lead | 4 tuần |
| T3 | Primary text **Taglish** | Primary text **English** | CTR + chi phí/lead | 4 tuần |
| T4 | CTA *Free Consultation* | CTA *Download treatment guide* | Chi phí/khách **đến khám** | 6 tuần |

⛔ **Không đo T1 bằng CPL.** Nêu tổng chi phí sẽ **làm CPL xấu đi** — lead ít hơn nhưng đúng người hơn. Đo bằng chi phí/khách đến khám, nếu không sẽ kết luận ngược.


===== kn-ho-so-thuong-hieu-sunwoo.md =====

# HỒ SƠ THƯƠNG HIỆU — SUNWOO AESTHETIC CENTER *(module swappable)*
Version 1.0 · Nguồn: <https://sunwooaesthetic.ph/> đọc ngày 2026-10-23 · Cập nhật 2026-10-23

> Đây là **module thương hiệu**. Đổi sang phòng khám khác = thay **file này** + `kn-rao-phap-ly-ph.md` (nếu đổi nước), **giữ nguyên bộ não**.
> Mọi ô `[CHỜ XÁC NHẬN]` phải do phía phòng khám điền **trước khi** chạy MODE 1. ⛔ Agent không được tự điền.

---

## 1 · Định danh

| Trường | Giá trị |
|---|---|
| **Tên** | Sunwoo Aesthetic Center |
| **Website** | <https://sunwooaesthetic.ph/> — **one-page WordPress**, không phải site nhiều trang |
| **Domain phụ nêu trên title** | `sunwoomedical.ph` — ⚠️ `[CHỜ XÁC NHẬN]` đây là domain chính hay domain cũ |
| **Địa chỉ** | Ground floor, 20 Upper McKinley Hill, Taguig, Metro Manila, Philippines |
| **Hotline** | +63 96 8885 8885 |
| **Kênh đang công bố** | Điện thoại · WhatsApp · Messenger · Facebook · Instagram · YouTube |
| **Định vị** | *"The trusted K-beauty destination in the Philippines"* · *"Seoul-standard aesthetics directly to Taguig"* |
| **Thị trường** | **Nội địa Philippines** — khách sống ở Metro Manila, tự đến phòng khám |

⚠️ **Đây KHÔNG phải mô hình du lịch y tế.** Khách không bay sang nước khác; họ lái xe hoặc đi Grab tới McKinley Hill. Mọi tri thức về visa, số ngày ở lại, đưa đón sân bay, phiên dịch — **không áp dụng**. Xem `kn-vung-philippines.md` §0.

---

## 2 · Sáu dịch vụ — đúng danh sách trong form đặt lịch

Form đặt lịch trên site có **6 lựa chọn**. Đây là danh sách chuẩn để đặt tên chiến dịch và nhóm quảng cáo:

| # | Dịch vụ (tên trên form) | Công nghệ/sản phẩm site nêu | Nhóm |
|---|---|---|---|
| ① | **Meso Hair Therapy** | mesotherapy tóc | Tóc |
| ② | **Skin Rejuvenation** | Filler · HA Collagen Booster | Da — trẻ hoá |
| ③ | **Xline Thread Lift** | chỉ nâng Xline | Nâng cơ — giá trị ca cao nhất |
| ④ | **Acne Treatment** | — | Da — bệnh lý |
| ⑤ | **Melasma Treatment** | **PicoSure Pro** | Da — sắc tố |
| ⑥ | **Scar Treatment** | — | Da — bệnh lý |

**Đặc điểm chung quyết định cách chạy ads:** cả 6 đều là **thủ thuật không phẫu thuật / xâm lấn tối thiểu**, phần lớn cần **nhiều buổi** và **có thời hạn hiệu quả**. Đây là lý do gói này có rào cản **BỀN** thay cho rào cản XA của gói quốc tế — xem `kn-chan-dung-hanh-trinh-ph.md` §2.

`[CHỜ XÁC NHẬN]` cho **từng** dịch vụ, và không có thì không chạy MODE 1:
- Số buổi trong một liệu trình
- Giá một buổi và giá trọn gói (PHP)
- Downtime thực tế (giờ/ngày)
- Hiệu quả kéo dài bao lâu, bao lâu nhắc lại
- Chống chỉ định / ai không làm được

---

## 3 · Hai bác sĩ — tài sản quảng cáo mạnh nhất chưa được dùng

| Bác sĩ | Vai trò | Bằng cấp site công bố |
|---|---|---|
| **Dr. Emanuel F. Gatdula** | Dermatologist | Doctor of Medicine · **Board-Certified Dermatologist** · **Diplomate, Philippine Dermatological Society (PDS)** · 3 năm nội trú Da liễu tại **RITM** · Licensed Physician (PRC) · former Licensed Medical Technologist · Certificate Basic Dermatologic Surgery · đào tạo nâng cao *Laser Systems and Energy-based devices* · tốt nghiệp De La Salle Medical and Health Sciences Institute |
| **Dr. Sharmaine Esquilona** | Aesthetic Physician | Doctor of Medicine · Licensed Physician (PRC) · 5+ năm lâm sàng · **Certificate in Aesthetic Medicine (Level I), AMI Philippines** · đào tạo Botulinum Toxin, Dermal Fillers, Thread Lifting, PRP, Chemical Peels, IPL/Diode Laser · **nói được English, Filipino và Masbateño** · tốt nghiệp FEU-NRMF |

**Ba thứ dùng được ngay trong quảng cáo, và đối thủ phần lớn không có:**
1. **Diplomate PDS** — ở Philippines đây là tín hiệu phân biệt rõ nhất giữa *derm clinic có bác sĩ da liễu* và *beauty clinic không có*. Khách PH có biết PDS. Đây là bằng chứng gỡ rào **NGỜ** mạnh hơn bất kỳ câu chữ nào.
2. **PRC license** — nêu được là nêu, vì luật PH cấm người không có giấy phép quảng cáo dịch vụ y khoa (`kn-rao-phap-ly-ph.md` §2).
3. **Nói được Filipino** — dùng cho nhóm khách không thoải mái tư vấn bằng tiếng Anh. Xem phần Taglish ở `kn-vung-philippines.md` §4.

⛔ **Không dùng tên bác sĩ kèm lời chứng thực kết quả của khách** — xem `kn-rao-phap-ly-ph.md` §3.

---

## 4 · Năm đặc quyền site đang công bố

Free expert consultation · Luxury private suites · **Written guarantee** · 24/7 care coordinator · Five-star aftercare

| Đặc quyền | Dùng trong ads thế nào |
|---|---|
| **Free consultation** | ★ CTA mạnh nhất của gói này. Micro-conversion rẻ, hạ rào NGẠI. Đưa lên headline được |
| **Luxury private suites** | Gỡ nỗi ngại riêng tư — rất thật với khách trị **mụn** và **rụng tóc** |
| **24/7 care coordinator** | Gỡ rào SỢ hậu thủ thuật |
| **Five-star aftercare** | Dùng kèm con số buổi tái khám, ⛔ không dùng như tính từ suông |
| 🔴 **Written guarantee** | ⛔ **KHÔNG đưa vào quảng cáo khi chưa có T&C bằng văn bản.** Xem §6 lỗi ③ |

---

## 5 · Con số site đang công bố

| Con số | Ghi trên site | Trạng thái |
|---|---|---|
| **300++** | "Board-certified doctors" | 🔴 **SAI RÕ RỆT** — xem §6 lỗi ① |
| **3000** | "Treatments performed" | `[CHỜ XÁC NHẬN]` mốc thời gian tính từ đâu |
| **98%** | "Client satisfaction" | `[CHỜ XÁC NHẬN]` đo bằng gì, cỡ mẫu bao nhiêu, kỳ nào |

⛔ **Agent không được dùng ba con số này trong quảng cáo cho tới khi có nguồn.** Một con số không chứng minh được vừa là rủi ro ASC/FDA (`kn-rao-phap-ly-ph.md`), vừa là thứ khách PH đọc xong bớt tin — không phải thêm tin.

---

## 6 · 🔴 Sáu lỗi đang có trên trang production — phát hiện 2026-10-23

Đây là phần **phải đọc trước khi chạy bất kỳ chiến dịch nào**, vì landing là nơi tiền quảng cáo đổ về.

| # | Lỗi | Vì sao nghiêm trọng | Sửa thế nào |
|---|---|---|---|
| ① | **"300++ Board-certified doctors"** trong khi site chỉ nêu **2 bác sĩ** | Khách đọc xong mất tin cả trang. Và đây là claim không chứng minh được → rủi ro ASC + Meta | Đổi thành con số thật, hoặc đổi nhãn sang thứ đếm được: *"3.000+ treatments performed"* |
| ② | **FAQ nói có "dental, plastic surgery and wellness services"** nhưng dịch vụ công bố chỉ là da liễu – thẩm mỹ nội khoa | Quảng cáo dịch vụ ngoài phạm vi giấy phép là rủi ro pháp lý nặng nhất ở PH | `[CHỜ XÁC NHẬN]` phạm vi giấy phép thật. Chưa xác nhận → **xoá khỏi FAQ** |
| ③ | **"Written guarantee"** cho kết quả thẩm mỹ y khoa | Bảo đảm kết quả điều trị là vùng cấm của quảng cáo y tế | Đổi sang bảo đảm **quy trình**: số buổi đã cam kết, chính sách làm lại nếu chưa đạt mốc kỹ thuật — có T&C văn bản |
| ④ | **"#1 K-beauty Medical Aesthetic Center in Philippines"** | Tuyên bố tối cao cần bằng chứng theo chuẩn ASC | Đổi sang định vị không so sánh thứ bậc: *"Korean-standard aesthetic care in BGC"* |
| ⑤ | **Lời chứng thực nêu tên + ảnh trước/sau** | Khách PH thấy được, nhưng đây là vùng bị siết cả bởi quy tắc đạo đức nghề y PH lẫn chính sách nền tảng | Giữ trên site nếu hợp lệ, ⛔ **không bê nguyên vào creative quảng cáo** cho tới khi rà §3 file pháp lý |
| ⑥ | **Kênh chat đang đẩy WhatsApp** | Ở Philippines, **Messenger và Viber** mới là đường nhắn tin phổ biến; WhatsApp yếu hơn hẳn. `[CHỜ XÁC NHẬN]` bằng số liệu thật của phòng khám | Đo tỷ lệ phản hồi theo từng kênh trong 4 tuần rồi mới đổi thứ tự nút |

> **Lỗi ① và ② là cổng chặn.** Agent **không xuất bất kỳ mẫu quảng cáo nào** dẫn về trang còn hai lỗi này — tiền đổ vào một trang tự mâu thuẫn là tiền mất, và lỗi ② có thể thành vấn đề giấy phép.

---

## 7 · Form đặt lịch hiện tại — 4 trường

`Your name` · `Phone (+63)` · `Service of interest` (6 lựa chọn) · `Your area` (gợi ý: BGC, Makati, Pasig…)

**Trường `Your area` là thứ làm đúng nhất trên trang này.** Nó chính là trường quyết định của gói nội địa: khách ở đâu quyết định họ có đến được McKinley Hill không. Xem `kn-vung-philippines.md` §2.

⚠️ Nhưng nó đang là **ô text tự do** → dữ liệu về sẽ lộn xộn, không cắt báo cáo theo vùng được.
**Đề xuất:** đổi thành dropdown theo đúng 4 vành đai ở `kn-vung-philippines.md` §2, kèm một ô *Other*. Có thế thì MODE 4 mới chẩn đoán được theo vùng.

**Dòng bảo mật trên form:** *"Your information is protected under the Data Privacy Act and used only to contact you for your consultation."* — đúng hướng, nhưng xem `kn-rao-phap-ly-ph.md` §4 cho phần còn thiếu.

---

## 8 · `[CHỜ XÁC NHẬN]` — bảng việc phải điền trước khi chạy

| # | Trường | Ai điền | Chặn mode nào |
|---|---|---|---|
| 1 | Giá từng dịch vụ + giá trọn gói (PHP) | Phòng khám | **1 · 2 · 3** |
| 2 | Số buổi / liệu trình, hiệu quả kéo dài bao lâu | Bác sĩ | **1 · 2 · 3** |
| 3 | Downtime thực tế từng dịch vụ | Bác sĩ | **2 · 3** |
| 4 | Phạm vi giấy phép thật của cơ sở | Pháp chế | **tất cả** |
| 5 | T&C "written guarantee" bằng văn bản | Pháp chế | **2 · 3** |
| 6 | Nguồn của 3000 / 98% | Marketing | **2 · 3** |
| 7 | Ngân sách/tháng (PHP) + CPL mục tiêu | Chủ đầu tư | **1 · 4** |
| 8 | Giá trị ca trung bình theo dịch vụ | Kế toán | **1 · 4** |
| 9 | Giờ mở cửa · có làm cuối tuần không | Vận hành | **2 · 3** |
| 10 | Có hỗ trợ trả góp / thẻ không | Vận hành | **2 · 3** — xem rào NGẠI |

⛔ Thiếu mục 4 thì **không chạy mode nào**. Thiếu mục 1–2 thì không chạy MODE 1/2/3 nhưng vẫn chạy được MODE 4 trên số liệu đã có.


===== kn-khung-landing-ph.md =====

# KHUNG LANDING L1–L5
Version 1.0 · Cập nhật 2026-10-23

---

## 1 · Chọn khung theo CHẶNG, không theo dịch vụ

| Khung | Chặng | Rào gỡ | Dùng khi | CTA chính |
|---|---|---|---|---|
| **L1 · So sánh cách làm** | S2 | NGỜ | Khách chưa chọn phương pháp | Tải bộ tiêu chí so sánh |
| **L2 · Trả lời thẳng** | S3 | **SỢ** | Khách đang sợ đau / biến chứng | Tải bộ câu hỏi cho bác sĩ |
| **L3 · Liệu trình & chi phí ★** | **S4** | **BỀN** | ★ Trang quan trọng nhất của gói này | Tải bảng liệu trình (PDF) |
| **L4 · Đặt lịch** | S5 | NGẠI | Khách đã chọn, đang chọn nơi | Đặt lịch tư vấn miễn phí |
| **L5 · Cộng đồng Hàn** | S5 | NGỜ | Nhóm N1, tiếng Hàn | KakaoTalk / đặt lịch |

⛔ **Một trang gỡ một rào.** Trang gỡ cả bốn là trang không gỡ rào nào.
⛔ **Không đổ mọi chiến dịch về trang chủ.** Trang chủ one-page hiện tại phục vụ S5; đổ S3 và S4 về đó là lãng phí toàn bộ phần phễu trên.

---

## 2 · Mười bốn khối — thư viện dùng chung

| Mã | Khối | L1 | L2 | **L3** | L4 | L5 |
|---|---|:-:|:-:|:-:|:-:|:-:|
| B01 | Hero — câu khách tự hỏi | ● | ● | ● | ● | ● |
| B02 | Trả lời ngắn ngay dưới hero | ● | ● | ● | ○ | ● |
| B03 | So sánh phương pháp (bảng trung lập) | ● | ○ | ○ | — | ○ |
| B04 | Quy trình từng bước + cảm giác thật | — | ● | ● | ○ | ● |
| B05 | Bác sĩ — **PDS · PRC · đào tạo** | ○ | ● | ● | ● | ● |
| B06 | Thiết bị — tên + đăng ký FDA PH | ○ | ● | ○ | ○ | ● |
| **B07** | ★ **Số buổi trong liệu trình** | — | ○ | **●** | ○ | ● |
| **B08** | ★ **Tổng chi phí trọn gói (PHP)** | — | — | **●** | ● | ● |
| **B09** | ★ **Hiệu quả giữ bao lâu + chi phí duy trì** | — | ○ | **●** | ○ | ● |
| B10 | Downtime bằng giờ/ngày | ○ | ● | ● | ● | ● |
| B11 | Ai **không** nên làm (chống chỉ định) | ○ | ● | ● | ○ | ● |
| B12 | Vị trí + chỉ đường + đỗ xe + giờ mở cửa | ○ | ○ | ○ | ● | ● |
| B13 | Micro-conversion (đặt **trước** form) | ● | ● | ● | ● | ● |
| B14 | Form 4 trường + miễn trừ + bảo mật | ○ | ● | ● | ● | ● |

● bắt buộc · ○ tuỳ chọn · — không dùng

> **B07 · B08 · B09 là ba khối làm nên gói này.** Trang L3 thiếu một trong ba → ⛔ không xuất.

---

## 3 · ★ L3 — trang quan trọng nhất, dựng chi tiết

Đây là trang trả lời rào **BỀN**, chặng **S4** — chặng cạnh tranh thấp nhất và gần như không đối thủ nào làm.

**Thứ tự khối, không đảo:**

```
B01  Hero       "How many sessions do you actually need?"
B02  Trả lời ngắn ngay: một con số khoảng, trong 2 dòng
B07  Bảng liệu trình: buổi 1 làm gì → buổi 2 → … → mốc nào thấy kết quả
B08  Tổng chi phí: giá/buổi VÀ giá trọn gói. ⛔ Không chỉ nêu "starts at"
B09  Giữ được bao lâu + nhịp duy trì + chi phí duy trì/năm
B05  Ai làm: bác sĩ, bằng cấp
B11  Ai không nên làm
B10  Downtime
B13  Micro: tải bảng liệu trình PDF
B14  Form
```

**Phép thử trước khi xuất L3:**
> *"Đọc xong trang này, khách có tự tính được mình tốn bao nhiêu trong 12 tháng tới không?"*
> Chưa → trang chưa xong.

⛔ **Không xuất L3 khi chưa có `[CHỜ XÁC NHẬN]` mục 1–2** (giá và số buổi). Một trang liệu trình điền số bịa còn tệ hơn không có trang.

---

## 4 · Luật viết từng khối

**B01 Hero** — câu **khách tự hỏi**, không phải câu phòng khám muốn nói.
✅ `"How long does a thread lift actually last?"`
⛔ `"Xline Thread Lift — Korean Technology at Sunwoo"`

**B02 Trả lời ngắn** — trả lời trong **2 dòng, ngay dưới hero**, trước mọi thứ khác. Khách PH cuộn nhanh; để câu trả lời ở giữa trang là mất họ.

**B05 Bác sĩ** — nêu **Diplomate PDS** và **PRC** bằng chữ, không bằng logo. Ở PH đây là tín hiệu phân biệt rõ nhất giữa *derm clinic* và *beauty spa*.

**B08 Chi phí** — nêu **cả hai số**: giá một buổi **và** giá trọn gói. Nêu một số là quay về đúng cái bẫy khách đã quen bị mắc.

**B11 Chống chỉ định** — khối này **tăng** niềm tin, không giảm. Nói rõ ai không nên làm là tín hiệu của cơ sở y khoa thật.

**B14 Form** — giữ đúng **4 trường** của form hiện tại. ⚠️ Đổi `Your area` thành **dropdown V1–V4**, nếu không MODE 4 không cắt được báo cáo theo vùng.

---

## 5 · Kỹ thuật — ba thứ quyết định ở Philippines

| Hạng mục | Yêu cầu | Vì sao ở PH |
|---|---|---|
| **Tốc độ mobile** | LCP < 2,5s trên **mạng 4G trung bình** | Phần lớn lưu lượng là mobile, mạng không ổn định. Trang nặng = mất khách trước khi đọc |
| **Click-to-call nổi** | Nút gọi + Messenger **dính đáy màn hình** | Nhiều khách PH chốt qua gọi/nhắn, không qua form |
| **Chỉ đường + đỗ xe** | Nhúng bản đồ + ghi rõ chỗ đỗ xe | McKinley Hill khó tìm chỗ đỗ. Đây là lý do huỷ hẹn có thật |

⚠️ **Trang one-page hiện tại không đủ cho 5 khung.** Cần dựng thêm trang con theo chặng. Dựng L3 trước — đó là trang mang lại chênh lệch lớn nhất.

---

## 6 · Bốn lỗi landing hay gặp của ngành này

| Lỗi | Vì sao hỏng | Sửa |
|---|---|---|
| Đổ mọi chiến dịch về **trang chủ** | Trang chủ phục vụ S5; S3/S4 vào đó không tìm thấy câu trả lời rồi thoát | Mỗi chặng một trang |
| Nêu **"starts at ₱X"** rồi hết | Khách biết đó không phải tổng, nên không tin cả trang | B08 nêu cả hai số |
| Form **đặt đầu trang** | Xin số trước khi gỡ rào = xin quá sớm | Form sau B07–B09, micro trước form |
| Ảnh trước/sau **thay cho câu trả lời** | Ảnh gỡ được rào NGỜ, ⛔ không gỡ được rào BỀN | Ảnh là bổ sung, không phải nội dung chính |


===== kn-quy-trinh-tuan-ph.md =====

# QUY TRÌNH TUẦN & VẬN HÀNH
Version 1.0 · Cập nhật 2026-10-23

---

## 1 · Nhịp tuần

| Thứ | Việc | Ai | Thời lượng |
|---|---|---|---|
| **Hai** | Báo cáo 7 dòng tuần trước · chốt 3 việc tuần này | Ads | 45' |
| **Ba** | Rà **search terms** · thêm phủ định (ghi lý do vào JSON) | Ads | 30' |
| **Năm** | Rà **search terms** lần 2 *(Pha 1)* · kiểm creative frequency | Ads | 30' |
| **Sáu** | Đối chiếu **lead → booking → đến khám** với CRM | Ads + CSKH | 45' |
| **Hằng ngày** | Kiểm quảng cáo bị từ chối · kiểm chi hụt | Ads | 10' |

⚠️ **Thứ Sáu là buổi quan trọng nhất.** Đó là lúc duy nhất trong tuần nhìn thấy tầng ⑦ — và tầng ⑦ là tầng quyết định. Bỏ buổi này thì cả tuần chỉ đang tối ưu CPL.

---

## 2 · Trước khi bật chiến dịch — checklist 12 ô

```
PHÁP LÝ
[ ] 1  Phạm vi giấy phép đã xác nhận bằng văn bản
[ ] 2  Thiết bị/sản phẩm đã có số đăng ký FDA PH
[ ] 3  Mọi claim đã qua pháp chế
[ ] 4  Landing đã xoá lỗi ① và ② (300++ doctors · dental/plastic surgery)

GEO
[ ] 5  Mọi chiến dịch đặt Presence / "People living in this location"
[ ] 6  Danh sách vùng loại trừ đã nạp (V4 + ngoài Metro)

DỮ LIỆU
[ ] 7  Ba tag CRM (vung · dich_vu · chang) đã gắn và test thật
[ ] 8  Bốn định nghĩa (lead hợp lệ · rác · booking · đến khám) đã chốt văn bản
[ ] 9  Pixel KHÔNG gửi tham số dịch vụ

NỘI DUNG
[ ] 10 Mỗi chặng có landing riêng, ⛔ không đổ chung trang chủ
[ ] 11 Trang L3 có đủ B07 · B08 · B09
[ ] 12 Có người trực Messenger trong giờ chạy quảng cáo
```

⛔ **Ô 1–4 trượt → không bật.** Ô 5–9 trượt → bật được nhưng **sẽ không chẩn đoán được gì**, và sáu tuần sau phải chạy lại từ đầu.

---

## 3 · Phân vai

| Vai | Sở hữu | ⛔ Không sở hữu |
|---|---|---|
| **Ads** | Bid · ngân sách · từ khoá · phủ định · creative · geo | Nội dung y khoa · giá |
| **Bác sĩ** | Số buổi · downtime · chống chỉ định · mọi phát ngôn chuyên môn | Câu chữ quảng cáo |
| **Pháp chế** | Duyệt claim · phạm vi giấy phép · quyền riêng tư | Chỉ số |
| **CSKH / trực page** | Phản hồi lần đầu · nhắc lịch · ghi tag CRM | Quyết định tắt/bật chiến dịch |
| **Agent AI** | Nghiên cứu từ khoá · sinh mẫu · chấm bảng · chẩn đoán · báo cáo | ⛔ Bật/tắt chiến dịch · ⛔ tiêu tiền · ⛔ phát ngôn y khoa |

> **Agent chỉ GỢI Ý, người duyệt trước khi chạy.** AI không thao tác trực tiếp trên tài khoản quảng cáo ở Pha 1.

---

## 4 · Thời gian phản hồi lần đầu — chỉ số ngầm quyết định CPL

Ở Philippines, phần lớn khách chốt qua **Messenger**, và họ nhắn **ngoài giờ hành chính**.

| Khung giờ | Vì sao quan trọng |
|---|---|
| **12:00–13:00** | Giờ nghỉ trưa dân văn phòng BGC |
| ★ **20:00–23:00** | Khung nhắn tin mạnh nhất. Không có người trực = mất lead đã trả tiền |
| **Thứ Bảy** | Ngày khách rảnh đi khám nhất |

⚠️ **Chạy quảng cáo 24/7 mà chỉ trực 9–18 giờ là trả tiền cho lead rồi bỏ.**
Hai cách xử lý, chọn một: ① giới hạn lịch chạy quảng cáo theo giờ trực · ② mở ca trực tối. ⛔ Không có cách thứ ba.

`[CHỜ XÁC NHẬN]` giờ trực thật của phòng khám và của đội page.

---

## 5 · Mỗi tháng — ba việc

1. **Rà lại ngưỡng.** Mã cảnh báo nào bắn nhiều mà không ai xử lý được → nới hoặc bỏ. Ngưỡng tốt là ngưỡng **≥ 70% cảnh báo dẫn tới một thao tác thật**.
2. **Cập nhật `[CHỜ XÁC NHẬN]`.** Giá đổi, liệu trình đổi, bác sĩ đổi → sửa `kn-ho-so-thuong-hieu-sunwoo.md`, ⛔ không sửa bộ não.
3. **Tra lại chính sách nền tảng và quy định PH.** Cả hai đổi theo thời điểm. Ghi ngày tra vào `kn-rao-phap-ly-ph.md`.

---

## 6 · Mỗi quý — một việc

**Đọc lại bốn rào cản bằng dữ liệu thật**, không bằng giả định:
- Lead rụng nhiều nhất ở câu hỏi nào trong hội thoại Messenger?
- Khách huỷ hẹn nêu lý do gì?
- Khách đến khám nhưng không chốt nói gì?

Nếu dữ liệu cho thấy rào nặng nhất **không phải BỀN** mà là NGẠI (giá) hay NGỜ (chuyên môn) → **sửa trọng số ngân sách giữa các chặng**, và sửa `kn-chan-dung-hanh-trinh-ph.md`.

⛔ Không giữ giả định ban đầu quá một quý mà không đối chiếu dữ liệu. Giả định của file này là **giả định khởi động**, không phải kết luận.


===== kn-rao-phap-ly-ph.md =====

# RÀO PHÁP LÝ & CHÍNH SÁCH NỀN TẢNG — PHILIPPINES
Version 1.0 · Cập nhật 2026-10-23 · **rà mọi output trước khi xuất**

> ⚠️ **File này là hướng dẫn vận hành, không phải tư vấn pháp lý.** Mọi mục đánh dấu 🔴 phải được **luật sư hoặc pháp chế của phòng khám xác nhận** trước khi chạy tiền thật. Quy định và chính sách nền tảng **đổi theo thời điểm** — tra lại nguồn gốc trước mỗi quý.

---

## 0 · HAI TẦNG RÀO — kiểm cả hai, không thay thế nhau

| Tầng | Áp vì | Hậu quả nếu sai |
|---|---|---|
| ① **Luật Philippines** | Cơ sở ở PH, dịch vụ là khám chữa bệnh | Phạt · đình chỉ · vấn đề giấy phép hành nghề |
| ② **Chính sách nền tảng** | Meta · Google · TikTok áp policy riêng | Tắt quảng cáo · khoá tài khoản quảng cáo · mất lịch sử học máy |

⚠️ **Qua tầng ② không có nghĩa là qua tầng ①.** Meta duyệt một mẫu quảng cáo không có nghĩa là mẫu đó hợp pháp ở Philippines. Và ngược lại: một câu hợp pháp hoàn toàn vẫn có thể bị Meta chặn.

---

## 1 · 🔴 Cơ quan và văn bản phải tra

| Cơ quan | Phạm vi | Liên quan gì tới gói này |
|---|---|---|
| **FDA Philippines** (RA 9711 — FDA Act of 2009) | Quảng cáo, khuyến mại **health product** | Thiết bị laser, filler, chỉ nâng, thuốc tiêm đều là health product. Quảng cáo health product **phải được FDA duyệt trước khi đăng**, và **không được nêu công dụng ngoài nhãn đã được duyệt** |
| **DOH** | Chính sách ngành y tế | Phạm vi hoạt động của cơ sở |
| **PRC** (Professional Regulation Commission) | Giấy phép hành nghề bác sĩ | **Người không có giấy phép không được quảng cáo dịch vụ y khoa.** Diễn viên đóng vai bác sĩ để chứng thực là vùng cấm |
| **ASC** (Ad Standards Council) | Tự quản ngành quảng cáo, **duyệt trước khi phát** | Tuyên bố tối cao (*"#1"*, *"best"*) phải có bằng chứng theo chuẩn ASC |
| **NPC** (RA 10173 — Data Privacy Act) | Dữ liệu cá nhân | Form thu số điện thoại + **dịch vụ quan tâm** = dữ liệu sức khoẻ, thuộc nhóm nhạy cảm |
| **DTI** (RA 7394 — Consumer Act) | Quảng cáo sai sự thật | Con số không chứng minh được |

🔴 **Ba câu hỏi phải có câu trả lời bằng văn bản trước khi tiêu đồng đầu tiên:**
1. Cơ sở được cấp phép **đúng những dịch vụ nào**? (chặn lỗi ② ở hồ sơ thương hiệu)
2. Thiết bị và sản phẩm dùng (PicoSure Pro, filler, chỉ Xline) **đã đăng ký FDA PH chưa**, số đăng ký bao nhiêu?
3. Mẫu quảng cáo health product có **cần FDA duyệt trước** không, và quy trình nộp ra sao?

⛔ Chưa có ba câu trả lời này → agent **chỉ được xuất bản nháp có đóng dấu `[CHỜ PHÁP CHẾ DUYỆT]`**, không xuất bản chạy được.

---

## 2 · CHECKLIST 12 Ô — chạy trước mọi output

| # | Ô kiểm | Loại thẳng nếu |
|---|---|---|
| ① | **Trong phạm vi giấy phép** | Quảng cáo dịch vụ cơ sở không được cấp phép |
| ② | **Không cam kết kết quả** | *"guaranteed"* · *"permanent"* · *"100%"* · *"no side effects"* |
| ③ | **Không tuyên bố tối cao thiếu bằng chứng** | *"#1"* · *"best in the Philippines"* · *"most advanced"* không có nguồn |
| ④ | **Số liệu có nguồn** | Con số nào không truy được về chứng từ |
| ⑤ | **Không chê ngoại hình người xem** | *"Are you embarrassed by your acne?"* |
| ⑥ | **Không chẩn đoán trong quảng cáo** | Quảng cáo kết luận tình trạng người xem |
| ⑦ | **Thiết bị/sản phẩm nêu đúng tên đã đăng ký** | Tên thương mại không khớp đăng ký FDA |
| ⑧ | **Không dùng chứng thực sai quy tắc nghề y** | Người không phải bác sĩ đóng vai bác sĩ · bác sĩ chứng thực kết quả lâm sàng |
| ⑨ | **Ảnh trước/sau có miễn trừ** | Thiếu *"Individual results may vary"* và thiếu điều kiện chụp |
| ⑩ | **Form có thông báo quyền riêng tư** | Thiếu mục đích · thời gian lưu · cách rút lại đồng ý |
| ⑪ | **Không nhắm theo tình trạng sức khoẻ** | Dùng thuộc tính sức khoẻ để target |
| ⑫ | **Có thông tin nhận dạng cơ sở** | Thiếu tên cơ sở · địa chỉ · hotline |

**Ô ①②③⑦ không đạt → loại thẳng**, không bù bằng phần nội dung hay.

---

## 3 · 🔴 Lời chứng thực và ảnh trước/sau

Đây là vùng **vừa bị luật PH siết, vừa bị nền tảng siết**, và trang production đang dùng cả hai.

| Hạng mục | Luật PH | Nền tảng (2026) |
|---|---|---|
| Lời chứng thực của khách | 🔴 Cần pháp chế xác nhận trong phạm vi quy tắc đạo đức nghề y | Cho phép nếu **không kèm claim bị cấm** |
| Bác sĩ chứng thực kết quả | 🔴 **Vùng cấm** theo quy tắc nghề nghiệp | — |
| Diễn viên đóng vai bác sĩ | 🔴 **Cấm** | Cấm |
| Ảnh trước/sau | 🔴 Cần miễn trừ + điều kiện chụp | Meta từ 2026 **cho phép** với đối tượng 18+, nhưng ⛔ cấm *"statements of inferiority about physical appearance"* đi kèm |

**Luật làm việc cho gói này:**
1. Giữ lời chứng thực **trên website** nếu pháp chế duyệt.
2. ⛔ **Không bê nguyên vào creative quảng cáo** — trang web và quảng cáo chịu hai bộ quy tắc khác nhau.
3. Ảnh trước/sau nếu dùng: cùng góc · cùng ánh sáng · cùng khoảng cách · không filter · có miễn trừ *"Individual results may vary with condition and treatment plan"* **in trên ảnh**, không chỉ ở caption.
4. ⛔ Không ghép ảnh trước/sau **của người khác** làm minh hoạ cho dịch vụ.

---

## 4 · Data Privacy Act — form đang thiếu gì

Form hiện tại ghi: *"Your information is protected under the Data Privacy Act and used only to contact you for your consultation."*

Đúng hướng. Nhưng trường **`Service of interest`** biến dữ liệu này thành **dữ liệu sức khoẻ** — thuộc nhóm thông tin nhạy cảm, yêu cầu cao hơn.

🔴 **Bốn thứ cần pháp chế bổ sung:**
1. **Đồng ý rõ ràng** cho việc xử lý thông tin nhạy cảm, tách khỏi đồng ý nhận marketing.
2. **Thời gian lưu trữ** và cách xoá.
3. **Cách rút lại đồng ý** — kênh nào, bao lâu.
4. Nêu rõ có **chia sẻ cho bên thứ ba** không (pixel, CRM, tổng đài thuê ngoài).

⛔ **Không gửi `Service of interest` vào pixel quảng cáo.** Gửi tình trạng sức khoẻ sang nền tảng quảng cáo vừa vi phạm chính sách nền tảng, vừa là rủi ro NPC. Chỉ gửi sự kiện *"Lead"* không kèm tham số dịch vụ.

---

## 5 · Chính sách nền tảng 2026 — cách viết cho qua

### Meta — từ 7/2026 xét theo **claim**, không theo sản phẩm

| ⛔ Không viết | ✅ Viết thế này |
|---|---|
| *"Are you struggling with hair loss?"* | *"Hair restoration options from board-certified doctors"* |
| *"Tired of looking old and tired?"* | *"Thread lift: what it does and how long it lasts"* |
| *"Eliminate melasma permanently"* | *"Melasma treatment plans — what results to expect"* |
| Ảnh cận cảnh véo mỡ, chỉ vào khuyết điểm | Chân dung bình thường, ánh sáng đều |

**Luật một dòng:** quảng cáo **nói về dịch vụ**, ⛔ không **nói về khuyết điểm của người xem**. Chuyển mọi câu hỏi *"Bạn có đang bị…"* thành câu trần thuật về dịch vụ.

### Google Ads

- ⛔ **Không nhắm theo tình trạng sức khoẻ**, không suy ra tình trạng của người dùng để cá nhân hoá.
- Nội dung điều trị mang tính thử nghiệm / chưa được chứng minh: ⛔ cấm.
- Một số danh mục y tế cần chứng nhận riêng. 🔴 `[CHỜ XÁC NHẬN]` danh mục của phòng khám có thuộc nhóm cần chứng nhận ở PH không.
- ★ Google Ads là nơi chạy S3–S5 của gói này, và yêu cầu ở đây **nhẹ hơn Meta** vì người dùng chủ động gõ tìm.

### TikTok
Siết chặt nhất trong ba nền tảng với nội dung y tế/thẩm mỹ. ⚠️ Dùng cho **nhận biết**, ⛔ không dùng cho chốt. Đừng đặt kỳ vọng lead ở đây.

---

## 6 · Khối miễn trừ chuẩn — dán vào mọi landing

```
Results vary from person to person and depend on skin condition, age and treatment plan.
A consultation with our licensed physician is required before any treatment.
Sunwoo Aesthetic Center · Ground floor, 20 Upper McKinley Hill, Taguig · +63 96 8885 8885
```

Bản Taglish cho creative mạng xã hội — ⛔ chỉ dùng cho phần dẫn, **không** dùng cho câu miễn trừ (câu miễn trừ luôn giữ English chuẩn).

---

## 7 · Bảng từ cấm — rà trước khi xuất

⛔ **Tuyệt đối không dùng**, dưới mọi cách diễn đạt và mọi ngôn ngữ:

| Nhóm | Từ |
|---|---|
| Cam kết | guaranteed · guarantee results · 100% · permanent · forever · lifetime · no side effects · painless · zero risk |
| Tối cao | #1 · best · the most advanced · top clinic · leading · unmatched *(thiếu bằng chứng)* |
| Y khoa | cure · heal · eliminate · remove permanently · medically proven *(thiếu nguồn)* |
| Chê ngoại hình | ugly · embarrassed · ashamed · flawed · fix your face · problem skin |
| Ép buộc | last chance · only today · limited slots *(nếu không có thật)* |

⚠️ **"Written guarantee"** đang có trên trang production thuộc nhóm **Cam kết**. Xem hồ sơ thương hiệu §6 lỗi ③.

---

## 8 · Quy trình duyệt — ba cửa, không bỏ cửa nào

```
① Agent tự rà 12 ô   →   ② Pháp chế phòng khám duyệt   →   ③ Nền tảng duyệt
   (tự động)              (bắt buộc với mọi claim mới)      (tự động)
```

- Cửa ① trượt → agent **không xuất**.
- Cửa ② là cửa **không bỏ được**, kể cả khi gấp. Agent phải in kèm **danh sách claim cần duyệt** ở cuối mỗi output để pháp chế rà nhanh.
- Cửa ③ trượt → ⛔ **không sửa chữ cho lách qua**. Sửa lách là cách bị khoá tài khoản. Đọc lý do từ chối, sửa đúng chỗ vi phạm.

**Mẫu khối cuối mỗi output:**
```
CLAIM CẦN PHÁP CHẾ DUYỆT
1. "Diplomate, Philippine Dermatological Society" — cần bản scan chứng chỉ
2. "3.000+ treatments performed" — cần số liệu từ hệ thống, nêu kỳ tính
3. Tên thiết bị "PicoSure Pro" — cần số đăng ký FDA PH
```


===== kn-vung-philippines.md =====

# VÙNG & THỊ TRƯỜNG PHILIPPINES — PHÂN TẦNG THEO BÁN KÍNH ĐI LẠI
Version 1.0 · Cập nhật 2026-10-23

> File này thay cho `knowledge/kn-thi-truong-quoc-te.md` của gói **Agent-AdsOptimize-Kangnam-QT** (repo khác). **Logic đổi hẳn**, không phải dịch lại.

---

## 0 · ⚠️ Khác biệt lớn nhất so với gói quốc tế — đọc trước

| | Gói KN-QT (du lịch y tế) | **Gói PHI (phòng khám nội địa)** |
|---|---|---|
| Khách ở đâu | Nước khác, phải **bay sang** | **Sống ở Metro Manila**, tự đến |
| Tầng chia theo | Quốc gia · kiều bào · expat | **Bán kính đi lại tới McKinley Hill** |
| Rào cản thứ tư | **XA** — *"về nhà ai lo cho tôi"* | **BỀN** — *"hết tác dụng rồi tôi phải trả tiếp bao nhiêu"* |
| Chặng đặc thù | **S4 Kế hoạch chuyến đi** | **S4 Số buổi & tổng chi phí** |
| `geo_mode` | Presence+Interest (tầng A/B/C) | ⛔ **Presence, luôn luôn** |
| Đơn vị đo | Chi phí/khách **đến khám** | Chi phí/khách **đến khám** *(giống)* |

⛔ **Mọi tri thức về visa, số ngày ở lại, đưa đón sân bay, phiên dịch, múi giờ — KHÔNG áp dụng.**
Một landing nói về đón sân bay gửi cho một phụ nữ đang ở Makati là một landing hỏng.

---

## 1 · ⚠️ CỔNG GEO — ràng buộc cứng của gói này

> Phòng khám có **một cơ sở** ở Ground floor, 20 Upper McKinley Hill, Taguig. Khách phải **đến tận nơi**. Vì vậy:

**⛔ MỌI dòng từ khoá bắt buộc `geo_mode = Presence`.**

Để Google tự chọn (mặc định `Presence or interest`) → quảng cáo hiện cho người ở **Cebu, Davao, Dubai, bất kỳ ai từng tìm hiểu về Manila**. CPL trông rẻ đi rất nhiều, và **không ai trong số đó đến khám**.

> **Lỗi này im lặng.** Google Ads không cảnh báo. Nó chỉ hiện ra sau 6–10 tuần, dưới dạng: *"lead nhiều mà lịch hẹn không tăng"*.

Trên Meta tương đương là **"People living in this location"**, ⛔ không phải *"People recently in"* hay *"travelling in"*.

**Kiểm ở 4 chỗ:** §4 bộ não · tiêu chí ⑦ bảng chấm WIN · bước ③ MODE 3 · cổng GEO-TARGET trong generator.

---

## 2 · Bốn vành đai — phân tầng thật của gói này

Metro Manila không đo bằng kilômét, đo bằng **phút kẹt xe**. Cùng 8 km, giờ thấp điểm 15 phút, giờ cao điểm 70 phút. Đây là ràng buộc có thật và nó quyết định ai đến, ai không.

| Tầng | Vành đai | Khu vực | Thời gian tới McKinley Hill | Ý nghĩa với ads |
|---|---|---|---|---|
| **V1** | **Lõi** | BGC · McKinley Hill · Fort Bonifacio · Taguig | 5–15 phút | **Tầng dễ chốt nhất.** Bid cao nhất, chấp nhận CPL cao nhất. Đi khám buổi trưa được |
| **V2** | **Kề** | Makati · Pasay · Pateros · Mandaluyong · Pasig (Ortigas) | 20–45 phút | Tầng chủ lực về khối lượng. Cần **lý do đủ mạnh** để vượt C5/EDSA |
| **V3** | **Xa trong Metro** | Quezon City · Manila · Parañaque · Las Piñas · Muntinlupa (Alabang) · Marikina · Caloocan | 45–90 phút | ⚠️ Chỉ chạy cho dịch vụ **giá trị ca cao** (Thread Lift, liệu trình Melasma). ⛔ Không chạy dịch vụ một buổi giá thấp |
| **V4** | **Ngoài Metro** | Cavite · Laguna · Bulacan · Rizal · tỉnh khác · nước ngoài | 90 phút+ | ⛔ **Mặc định LOẠI.** Chỉ mở khi có bằng chứng ca thật đã đến từ đó |

**Ba luật của bảng này:**
1. **Ngân sách V1 + V2 ≥ 70%.** Đây không phải quy tắc tiết kiệm, đây là quy tắc *đi lại có thật*.
2. **V3 chỉ mở cho dịch vụ giá trị ca cao.** Một người ở Quezon City không vượt EDSA 70 phút để trị mụn một buổi — nhưng có thể vượt cho một ca Thread Lift.
3. **V4 phải chứng minh trước khi mở.** `[CHỜ XÁC NHẬN]` từ CRM: đã có bao nhiêu ca thật đến từ ngoài Metro Manila trong 6 tháng qua. Không có số → không mở.

⚠️ **Trường `Your area` trên form chính là trường cắt báo cáo theo bảng này.** Nó đang là ô text tự do → đổi thành dropdown V1/V2/V3/V4 + *Other*, nếu không MODE 4 không chẩn đoán được theo vùng.

---

## 3 · Ba nhóm khách đặc thù — không nằm trong vành đai

Ba nhóm dưới đây cắt ngang bốn vành đai, và **gói quốc tế không có nhóm nào trong số này**.

### N1 · Cộng đồng Hàn Quốc tại McKinley Hill ★
McKinley Hill có khu dân cư Hàn Quốc đáng kể ngay cạnh phòng khám. Với một phòng khám **định vị K-beauty**, đây là nhóm có độ khớp cao nhất và gần như chắc chắn **chưa ai chạy riêng**.

- Ngôn ngữ: **tiếng Hàn**, không phải English.
- Họ so sánh với phòng khám **ở Seoul**, không so với phòng khám PH → lập luận phải là *"chuẩn Seoul, ngay đây, không phải bay về"*.
- Kênh: **KakaoTalk** và nhóm cộng đồng, ⛔ không phải Messenger.
- `[CHỜ XÁC NHẬN]` phòng khám có nhân sự nói tiếng Hàn không. **Không có → không chạy nhóm này**, vì lead về không ai nghe máy được.
- Ngân sách đề xuất khi mở: **10–15%**, chạy riêng chiến dịch, riêng landing.

### N2 · Expat & nhân sự văn phòng BGC
BGC là lõi văn phòng đa quốc gia. Nhóm này tìm bằng tiếng Anh chuẩn, nhạy với **lịch hẹn ngoài giờ** và **downtime** hơn là nhạy giá.

- Thông điệp trục: *"vào buổi trưa, về làm việc buổi chiều"* — nếu downtime thật cho phép.
- ⛔ Không hạ giá cho nhóm này. Họ không mua vì rẻ.

### N3 · OFW & gia đình OFW
Người Philippines đi làm nước ngoài về phép, hoặc gia đình được gửi tiền về. Cửa sổ thời gian hẹp (về nước 2–4 tuần), ngân sách theo đợt.

- Mùa rõ rệt: **tháng 11–1** (Giáng sinh) và **tháng 4–5** (hè).
- ⚠️ Người **gõ tìm kiếm** có thể là người ở nước ngoài, nhưng người **điều trị** ở PH → đây là ngoại lệ duy nhất có thể cân nhắc nới `geo_mode`, và **chỉ sau khi** có dữ liệu chứng minh. Mặc định vẫn **Presence**.

---

## 4 · Ngôn ngữ — English, Taglish hay Filipino

Philippines dùng tiếng Anh là ngôn ngữ chính thức, nhưng **ngôn ngữ quảng cáo hiệu quả không phải tiếng Anh trang trọng**.

| Nơi dùng | Ngôn ngữ | Lý do |
|---|---|---|
| **Google Search ads** | English chuẩn | Người ta gõ tìm kiếm bằng English |
| **Landing page** | English chuẩn, câu ngắn | Trang y khoa cần giọng tin cậy |
| **Meta / TikTok creative** | ★ **Taglish** | Đây là giọng người PH nói thật trên mạng xã hội. English trang trọng đọc như brochure bệnh viện và bị lướt qua |
| **Kịch bản tư vấn Messenger** | **Taglish** | Dr. Esquilona nói được Filipino — đây là lợi thế có thật |
| **Nhóm N1 Hàn Quốc** | **Tiếng Hàn** | Không có người nói tiếng Hàn thì không mở nhóm này |

**Luật Taglish:** trộn ở mức **tự nhiên**, không gượng. *"Ready ka na ba for glass skin?"* đọc được. *"Ang galing ng aming teknolohiya"* dịch máy thì nghe giả. ⛔ Nếu không có người bản địa duyệt creative Taglish thì dùng English — giả giọng còn hại hơn.

⛔ **Không dùng Taglish trong**: tên dịch vụ y khoa · câu miễn trừ · thông tin giá · nội dung về chỉ định điều trị.

---

## 5 · Kênh — Philippines không giống Việt Nam

| Kênh | Vai trò | Ghi chú |
|---|---|---|
| **Facebook + Messenger** | ★ Kênh số 1 | Philippines thuộc nhóm thâm nhập Facebook cao nhất thế giới. Messenger là đường nhắn tin mặc định |
| **TikTok** | Khám phá · nhóm trẻ | Mạnh cho mụn, trẻ hoá da. Yếu cho Thread Lift (nhóm tuổi khác) |
| **Instagram** | Bằng chứng hình ảnh | Khách xem trước khi đặt lịch, ít khi là kênh chốt |
| **Google Search** | ★ Ý định cao nhất | Khối lượng nhỏ hơn Meta nhưng chất lượng lead cao hơn. Là nơi chạy S3–S5 |
| **Viber** | Nhắn tin phổ biến ở PH | `[CHỜ XÁC NHẬN]` phòng khám có dùng không |
| **WhatsApp** | ⚠️ Site đang đẩy | Yếu ở PH so với Messenger/Viber. Đo 4 tuần rồi quyết thứ tự nút |

**Hệ quả phân bổ:** gói này **không** giống gói Search-first của KN-QT. Đề xuất khởi đầu: **Meta 50–60% · Google Search 30–40% · TikTok 10%** cho pha học, rồi dịch chuyển theo chi phí/khách **đến khám**, ⛔ không theo CPL.

---

## 6 · Tiền tệ và cách nói giá

- Đơn vị: **PHP (₱)**. ⛔ Không quy đổi USD trong quảng cáo cho khách nội địa.
- Khách PH quen với **"starts at ₱X"** — nhưng đó cũng chính là cái bẫy của ngành này: quảng cáo giá một buổi rồi tư vấn mới lộ ra cần 6 buổi.
- ★ **Lợi thế cạnh tranh của gói này là nói thẳng tổng liệu trình.** Xem rào cản **BỀN** ở `kn-chan-dung-hanh-trinh-ph.md` §2 và chặng **S4** ở §3.
- `[CHỜ XÁC NHẬN]` có hỗ trợ trả góp / thẻ tín dụng không. Ở PH đây là đòn bẩy thật cho ca giá trị cao, nhưng ⛔ không nêu khi chưa có chính sách.

---

## 7 · Mùa vụ — lịch Philippines

| Thời điểm | Ảnh hưởng |
|---|---|
| **Tháng 11 – đầu tháng 1** | ★ Cao điểm: tiệc cuối năm, OFW về, thưởng 13th-month pay. **Chuẩn bị ngân sách từ tháng 10** |
| **Tháng 4 – 5** | Hè, mùa cưới, OFW về đợt hai |
| **Tháng 6 – 10** | Mùa mưa/bão. Ngày có bão → lưu lượng đi lại sập, **tạm dừng hoặc hạ bid**, đừng đọc số ngày đó như xu hướng |
| **Holy Week** | Metro Manila vắng, nhiều người về quê. Hạ ngân sách |
| **Payday 15 và 30** | ★ Chu kỳ chi tiêu rõ ở PH. Đẩy bid quanh hai mốc này và theo dõi riêng |

⛔ **Không kết luận xu hướng từ một tuần có bão hoặc một tuần lễ dài.** So sánh phải cùng loại ngày.


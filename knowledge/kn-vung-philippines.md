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

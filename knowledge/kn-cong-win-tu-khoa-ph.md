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

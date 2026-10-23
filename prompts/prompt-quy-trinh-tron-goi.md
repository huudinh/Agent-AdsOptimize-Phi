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

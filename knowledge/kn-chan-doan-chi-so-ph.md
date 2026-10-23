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

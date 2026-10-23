# MARKET CONFIG — schema file JSON sinh bộ từ khoá

Mỗi **bộ VÙNG × DỊCH VỤ** = **1 file JSON** trong thư mục này → **1 file `.xlsx` 5 sheet** trong `out/`.

> Gói KN-QT chia theo **thị trường (quốc gia)**. Gói này chia theo **VÙNG (bán kính đi lại) × DỊCH VỤ**, vì cùng một ca Thread Lift thì khách ở BGC và khách ở Quezon City có **ràng buộc đi lại, tỷ lệ đến khám và mức bid chấp nhận được** khác hẳn nhau.

```bash
pip install openpyxl
python tools/build_keyword_workbook.py markets/threadlift-v1-bgc.json
python tools/build_keyword_workbook.py "markets/*.json" -o out/
```

**Ví dụ hoàn chỉnh đã build được:** [`threadlift-v1-bgc.json`](threadlift-v1-bgc.json) — 5 chân dung · 5 chiến dịch · 5 landing · 17 từ khoá · phễu S1–S6. Dùng để đối chiếu khuôn.

> ⚠️ Khoá gốc vẫn tên là `zone` để dùng chung generator với các gói anh em. Trong gói này, `zone` **mô tả một bộ vùng × dịch vụ**.

---

## Trật tự bắt buộc khi điền — đây chính là phương pháp luận

```
zone → chan_dung → hanh_trinh → chien_dich → landing → tu_khoa → phu_dinh → nguong/lo_trinh
 ①       ②            ③            ④           ⑤          ⑥          ⑦            ⑧
```

① bộ này là **vùng nào × dịch vụ nào** · ② **ai** mua · ③ họ đi qua **chặng nào (S1–S6)** · ④ mỗi chặng cần **chiến dịch** gì · ⑤ mỗi chiến dịch đổ về **trang** nào · ⑥ người đó **gõ gì, từ đâu** · ⑦ chặn truy vấn lệch · ⑧ ngưỡng vận hành.

⛔ Đảo thứ tự = quay về cách làm cũ: gom từ khoá trước, gán người sau.

---

## ① `zone` — định danh bộ

| Khoá | Kiểu | Ghi chú |
|---|---|---|
| `ten` | string | Tên hiển thị, vd `"Xline Thread Lift · V1 · BGC – McKinley Hill"` |
| `ma` | string | slug nội bộ |
| `nganh` | string | vd `"Aesthetic · Dermatology (non-surgical)"` |
| `ten_file` | string | Tên file xuất, **không kèm `.xlsx`** |
| `ds_phu_dinh_chung` | string | Tên danh sách phủ định cấp tài khoản |
| `ngan_sach_thang` | number | Ô đầu vào (nền vàng) trên sheet 1 |
| `muc_tieu` | string | 1 câu, nêu **thứ tự ưu tiên chỉ số** — đặt *chi phí/khách đến khám* lên trước CPL |
| ★ `thuong_hieu` | string | In lên tiêu đề sheet 1. **Generator brand-neutral, đọc tên từ đây** |
| ★ `don_vi_tien` | string | vd `"PHP (₱)"`. Định dạng số không kèm ký hiệu nên dùng được mọi tiền tệ |
| ★ `markets` | string | Các vùng bộ này phục vụ, vd `"V1 + V2 ở Pha 2"` |
| ★ `tang` | string | `"V1 · lõi"` / `"V2 · kề"` / `"V3 · xa trong Metro"` / `"V4 · ngoài Metro"` |
| ★ `ngon_ngu` | string | vd `"English chuẩn (Search + landing) · Taglish (Meta + Messenger)"` |
| ★ `rui_ro_qc` | string | Mức rủi ro + cơ quan phải tra, vd `"🔴 CAO — health product theo RA 9711"` |
| ★ `claim_cam` | array | Claim cấm **riêng của thương hiệu**: `[{"tu": "...", "ly_do": "..."}]` — xem §9 |

---

## ② `chan_dung[]` — 4–7 chân dung

Khoá: `ma` · `ten` · `insight` · `rao_can` · `chang_vao` · `chien_dich` · `gia_tri_ca`.

**Hai điều bắt buộc trong `insight`:**
1. Viết bằng **lời khách**, trong ngoặc kép. *"Khách quan tâm giải pháp trẻ hoá"* là một câu rỗng.
2. Ghi rõ **người gõ có phải người điều trị không** và **vành đai V1–V4**.

`rao_can` là **một** trong: `SỢ` · `NGỜ` · `NGẠI` · **`BỀN`** + một câu giải thích.

> **Tách hẳn hai cặp:** ① khách lần đầu vs **khách đã làm ở nơi khác và không hài lòng** (nhóm sau trả được CPC cao nhất, cần bằng chứng về **người** chứ không phải về **máy**) · ② khách bản địa vs **cộng đồng Hàn tại McKinley Hill** (tìm bằng tiếng Hàn, so với Seoul, dùng KakaoTalk).

---

## ③ `hanh_trinh[]` — 6 chặng S1→S6

Đúng **6 phần tử**, theo thứ tự. KN-QT có 7 (chèn S4 chuyến đi); gói này có 6, và **S4 là chặng số buổi & tổng chi phí**.

Khoá: `chang` · `chan_dung` · `tam_ly` · `rao_can` · `chien_dich` · `tu_khoa` · `thong_diep` · `bang_chung` · `lp` · `chuyen_doi` · `sau_lead` · `kpi` · `tiep_theo`.

| Chặng | Dấu hiệu | Lưu ý |
|---|---|---|
| S1 Nhận biết | `what is` · `why am i` | Không chạy Search chốt |
| S2 So sánh cách làm | `vs` · `worth it` | ⛔ Không bán thương hiệu ở chặng này |
| S3 Nỗi sợ & an toàn | `side effects` · `painful` · `gone wrong` | Gọi tên nỗi lo rồi **trả lời ngay** |
| **S4 Số buổi & tổng chi phí ★★** | `how many sessions` · `how long does it last` · `total cost` · `maintenance` | **Chặng quyết định** — cạnh tranh thấp nhất |
| S5 Chọn nơi làm | `bgc` · `near me` · `book` | Bid cao nhất |
| S6 Sau điều trị | `aftercare` · `touch up` | Không ads; vẫn cần trang cho CRM/Messenger |

---

## ④ `chien_dich[]` + ⑤ `cap_uu_tien[]`

`chien_dich[]`: `ten` · `uu_tien` (khớp một `cap`) · `vai_tro` · `ty_trong` (**tổng đúng 1.0**) · `diem {y_dinh, gia_tri, kha_nang_chot}` (1–5) · `bid` · `chi_tieu`.

**Quy ước tên — khoá nối sang sheet 2 (`COUNTIF`) và sheet 5:**
```
PHI | <vùng> | <dịch vụ> | <chặng> | <cụm truy vấn>

PHI | V1 | ThreadLift | S4 | Sessions & Total Cost
PHI | V2 | ThreadLift | S4 | Sessions & Total Cost
PHI | V1 | Melasma    | S3 | Safety & Side Effects
```
Sửa tên ở một nơi phải sửa cả hai.

**Ngân sách tối thiểu:** `S3 ≥ 15%` · **`S4 ≥ 20%`** · `S5 ≥ 30%` · **`V1+V2 ≥ 70%`**. Chia theo **ý định mua × giá trị ca**, ⛔ không theo lượng tìm kiếm.

---

## ⑥ `landing[]`

`ma_ten` dạng **`LPx: tên trang`** — generator cắt phần trước dấu `:` làm mã đối chiếu với cột `lp`.

| Khoá | Ghi chú |
|---|---|
| `loai` | `L1 - So sánh cách làm` · `L2 - Trả lời thẳng` · `L3 - Liệu trình & chi phí` · `L4 - Đặt lịch` · `L5 - Cộng đồng Hàn` |
| `chang` | Chặng trang này phục vụ |
| `chan_dung` | Mã `CDx`, có thể nhiều |
| `rao_can` | Rào trang này **phải gỡ** — ⛔ không gỡ chung chung cả bốn |
| `noi_dung` | ★ Trang **L3 phải ghi rõ có đủ B07 (số buổi) · B08 (tổng chi phí) · B09 (giữ bao lâu + chi phí duy trì)** |
| `cta` · `micro` | Micro-conversion đặt **trước** form |

---

## ⑦ `tu_khoa[]` — 1 dòng = 1 từ khoá × 1 kiểu khớp × 1 vùng

Khoá: `chien_dich` · `nhom_qc` · `tu_khoa` · `khop` · **`market`** · **`geo_mode`** · `uu_tien` · `chang` · `chan_dung` · `rao_can` · `canh_tranh` · `win` · `lp` · `thong_diep` · `ghi_chu`.

| Trường | Luật |
|---|---|
| **`market`** | **V1 / V2 / V3 / V4** — người gõ **ĐANG Ở ĐÂU**, ⛔ không phải thành phố trong chuỗi từ khoá |
| **`geo_mode`** | ⛔ **Luôn là `Presence`.** Generator chặn nếu thiếu |
| `win` | Điểm cổng WIN dạng `3/4`. **< 3/4 → không đưa vào file** |
| `thong_diep` | Câu sẽ xuất hiện trong mẫu quảng cáo. **Cổng CLAIM quét ô này**, ⛔ không quét `tu_khoa` |

> ★ **Cùng một chuỗi từ khoá ở hai vùng là HAI dòng hợp lệ, không phải trùng lặp.**
> `how long does thread lift last` gõ từ V1 và gõ từ V2 cần bid khác và tỷ lệ đến khám khác.
> Generator tính trùng theo **(từ khoá × khớp × market)** — đã sửa so với bản KN-QT, bản đó chỉ tính (từ khoá × khớp) nên báo nhầm.

---

## ⑧ Phủ định · ngưỡng · lộ trình

`phu_dinh_chung[]` và `phu_dinh_cheo[]`: `nhom` · `tu` · `khop` · `ap_dung` · `ly_do`.
⛔ **Luôn ghi `ly_do`.** Không ghi thì ba tháng sau không ai biết vì sao chặn, và sẽ có người mở lại.

`nguong[]`: `quy_tac` · `he_so` · `moc` · `hanh_dong`.
`lo_trinh[]`: `pha` · `thoi_gian` · `dieu_kien` · `chien_luoc` · `chuyen_doi` · `bat_buoc`.

Các khối còn lại: `nguyen_tac[]` · `quy_trinh_phu_dinh[]` · `quy_tac_canh_tranh[]` · `ab_test[]` · `rui_ro[]` · `hook_format[]` · `phieu{}`.

**`phieu{}` — giá trị phải là SỐ**, `ghi_chu` là **dict** chú thích từng trường:
```json
"phieu": {
  "cpc": 60, "click_lead": 0.04, "lead_lich": 0.35,
  "show_up": 0.55, "chot": 0.30, "gia_tri_ca": 45000,
  "ghi_chu": { "cpc": "GIẢ ĐỊNH ĐẦU VÀO (₱)…", "…": "…" }
}
```
⚠️ Đây là **ô nền vàng — giả định đầu vào**, không phải số thật. Chạy 2 tuần rồi thay.

---

## ⑨ `claim_cam` — nơi khai claim cấm riêng của thương hiệu

Generator có **cổng CLAIM** chặn các claim rủi ro. Danh sách mặc định chỉ giữ những thứ rủi ro ở **mọi** thị trường: `lifetime warranty` · `guaranteed result` · `100% safe` · `no side effects` · `painless`…

Claim rủi ro **riêng theo thương hiệu hoặc theo nước** khai ở đây:
```json
"claim_cam": [
  { "tu": "written guarantee", "ly_do": "chưa có T&C văn bản — xem hồ sơ thương hiệu §6 lỗi ③" },
  { "tu": "#1 k-beauty",       "ly_do": "tuyên bố tối cao, cần bằng chứng chuẩn ASC" }
]
```

> **Vì sao tách ra:** gói KN-QT chặn cứng `board certified` trong code vì ở thị trường US/AU đó hay bị nhầm với tư cách hội. Với gói này thì ngược lại — bác sĩ **có** chứng nhận thật (Diplomate PDS), và đó là bằng chứng mạnh nhất để gỡ rào NGỜ. **Tri thức đó thuộc module thương hiệu, không thuộc generator.**

---

## ⑩ Bốn cổng generator tự chặn

| Cổng | Chặn gì |
|---|---|
| **GEO-TARGET** | Dòng từ khoá thiếu `market` hoặc `geo_mode` |
| **CLAIM** | `thong_diep` hoặc `nhom_qc` chứa claim cấm (mặc định + `claim_cam`) |
| **TỪ CẤM** | `thong_diep` chứa từ cấm quảng cáo y tế |
| **TRÙNG LẶP** | Trùng (từ khoá × khớp × market) |

Trượt cổng nào → **không xuất file**, in ra đúng dòng bị lỗi.

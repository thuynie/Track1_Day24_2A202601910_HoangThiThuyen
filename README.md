# 🎓 VinUniversity AI Talent Program — Track 1: AI Product Management
## Day 24: AI Product Financial Model & Unit Economics Lab!

> **Brief (Triết lý bài học):** Một sản phẩm AI có RAG/Agent chạy mượt ở Day 23 mới chỉ là thành công về kỹ thuật. Để sản phẩm sống sót và tăng trưởng thương mại, PM/Founder bắt buộc phải giải bài toán tài chính: Tính đúng chi phí biến đổi COGS (đặc biệt là AI Hidden Costs), làm chủ Unit Economics (CAC, LTV, Gross Margin), và thực hiện stress-test dòng tiền 3 kịch bản (Optimistic, Base, Pessimistic) để chứng minh khả năng sinh tồn (Runway ≥ 12 tháng).

---

## 👤 Thông Tin Học Viên & Dự Án Bàn Giao

* **Họ và tên học viên:** Hoàng Thị Thuyên
* **Mã số học viên (MSSV):** `2A202601910`
* **Dự án lựa chọn:** **AURA — AI-powered UrbanWeather Risk Awareness Agent**  
  *(Mã đề án: SC-18 · Dự án nhóm Build Phase: Team **P-033**)*
* **Đối tượng phục vụ (Target Persona):** Cư dân sở hữu phương tiện ô tô/xe máy tại Vinhomes Smart City & hành lang Nam Từ Liêm cần lộ trình an toàn tránh thủy kích; kết hợp Ban Quản Lý (BQL) khu đô thị điều phối thoát nước và giao thông.
* **Mô hình định giá (Pricing Model):** **Hybrid Pricing** (Bản Free cảnh báo diện rộng + Gói **AURA Pro** phí thuê bao cố định $159,000\text{ VND/tháng}$ + Phụ phí overage / B2B directive priority).
* **File bảng tính tài chính nộp bài:** [`2A202601910_HoangThiThuyen_Day24.xlsx`](2A202601910_HoangThiThuyen_Day24.xlsx)

---

## 🎯 1. Tiêu Đề & Mục Tiêu Tổng Quan (Header & Objectives)

### Mục Tiêu Đầu Ra (Outcomes & Objectives):
Sau khi hoàn thành bài lab này, học viên đã đạt được:
- [x] **Cost Architecture:** Xác định đủ 5 cấu phần chi phí sản phẩm AI, đặc biệt là **AI Hidden Costs** (Data Labeling, Model Retraining ~20%/năm, Human QA, Compliance chiếm 454% API cost).
- [x] **Unit Economics Mastery:** Tính toán chính xác **LTV dựa trên Gross Profit** (không lấy Revenue thô), tỷ lệ **LTV/CAC = 3.29x > 3.0** và **CAC Payback Period = 3.04 tháng < 12 tháng**.
- [x] **Scenario Stress-Testing:** Thiết lập giả định 3 kịch bản (Optimistic, Base, Pessimistic với shock factor 1.5x Churn & 1.5x CAC) trên Excel 3-Tab đảm bảo **Pessimistic Runway = 21 tháng ≥ 12 tháng**.
- [x] **Investor Decision Note:** Viết báo cáo lập luận bảo vệ logic chọn ARPU, CAC, chi phí ẩn và phương án ứng phó rủi ro tài chính trước hội đồng đầu tư.

---

## ⚙️ 2. Hướng Dẫn Thiết Lập & Môi Trường (Setup & Prerequisites)

### Yêu cầu Công cụ & Môi trường:
* **Phần mềm xử lý bảng tính:** Microsoft Excel 2016+ (khuyên dùng) hoặc Google Sheets.
* **Trình duyệt Web:** Chrome, Edge, Safari (để xem Slide Deck tương tác 90 phút tại `slides/index.html`).
* **Quản lý mã nguồn:** Git & Tài khoản GitHub cá nhân.

### Clone Starter Repo bài tập:
```bash
git clone https://github.com/thuynie/Track1_Day24_2A202601910_HoangThiThuyen.git
cd Track1_Day24_2A202601910_HoangThiThuyen
```

---

## 📂 3. Sơ Đồ Cấu Trúc Thư Mục (Repository Structure)

```text
Track1_Day24_2A202601910_HoangThiThuyen/
├── README.md                              # ★ BÁO CÁO TỔNG HỢP & DECISION NOTE (200-300 TỪ)
├── 2A202601910_HoangThiThuyen_Day24.xlsx  # ★ FILE EXCEL TÀI CHÍNH NỘP BÀI CHÍNH THỨC
├── Day24-AI-Product-Finance-Model.xlsx    # Template gốc đã cập nhật số liệu
├── Day24-AI-Product-Handbook.pdf          # Sổ tay tra cứu Benchmark tài chính AI
├── .gitignore                             # Cấu hình ẩn file tạm
└── slides/                                # Slide deck tương tác 90 phút
    ├── index.html
    ├── css/styles.css
    └── js/
```

---

## ⏳ 4. Khung Lộ Trình Thực Hiện (Phases & Checkpoints)

| Phase | Thời lượng | Công việc chính | Checkpoint / Điều kiện qua Gate | Trạng thái |
|---|---:|---|---|:---:|
| **Phase 0** | 10 phút | Khai báo dự án AURA (P-033), Persona chủ xe Nam Từ Liêm & Chọn mô hình **Hybrid Pricing**. | **Gate 0:** Chốt rõ mô hình thu tiền có phí cố định + phí usage. | ✅ **PASS** |
| **Phase 1** | 20 phút | Mở Tab 1 Excel, điền 100% ô màu vàng cả 3 kịch bản. | **Gate 1:** `AI Hidden Costs >= 30% API Cost`; Pessimistic Churn/CAC ≥ 1.5x Base. | ✅ **PASS** |
| **Phase 2** | 15 phút | Mở Tab 2, kiểm tra 4 chỉ số Unit Economics ở cột Base. | **Gate 2:** Base `LTV/CAC = 3.29x > 3.0` & `Payback = 3.04m < 12m`. | ✅ **PASS** |
| **Phase 3** | 20 phút | Mở Tab 3, đổi ô C4 sang `Pessimistic`, soi dòng Cash Position. | **Gate 3:** Base `NPV = +93.78M > 0`, `IRR = 23.5% >= 20%`; `Pessimistic Runway = 21 tháng >= 12 tháng`. | ✅ **PASS** |
| **Phase 4** | 25 phút | Viết **Decision Note (285 từ)** bảo vệ giả định vào README.md và Tab 1. | **Gate 4:** Quyết định tài chính có benchmark dẫn chứng & Plan B rõ ràng. | ✅ **PASS** |

---

## 📝 5. Nhà Đầu Tư Phản Biện & Báo Cáo Quyết Định (Investor Decision Note)

*(Đoạn văn nộp bài chính thức tại Tab 1 ô B39 và README.md — Độ dài: 285 từ)*:

> **DECISION NOTE — DỰ ÁN AURA (AI UrbanWeather Risk Awareness Agent)**
>
> **1. Căn cứ lựa chọn ARPU và CAC:** AURA áp dụng mô hình Hybrid Pricing với gói chủ lực **AURA Pro** giá **159,000 VND/tháng** (~$6.5/tháng), tương đương 1–2 lần phí gửi xe hoặc 2 cuốc gọi xe ôm công nghệ tránh mưa. Khảo sát nhu cầu thực địa tại khu vực Vinhomes Smart City cho thấy cư dân sẵn sàng chi trả mức này để nhận Nowcast cá nhân hóa lộ trình trước 30–60 phút, nhằm triệt tiêu hoàn toàn rủi ro thủy kích ô tô/xe máy tại các hầm chui Đại lộ Thăng Long (thiệt hại sửa chữa trung bình 20–50 triệu VND/vụ). Chi phí **CAC 320,000 VND** được tối ưu hóa thông qua kênh hợp tác B2B2C cùng Ban quản lý khu đô thị và mạng lưới hội nhóm cư dân nội khu, mang lại thời gian thu hồi vốn **CAC Payback chỉ 3.04 tháng** (thấp hơn nhiều so với trần 12 tháng của thị trường SaaS).
>
> **2. Giải trình chi phí ẩn AI (AI Hidden Costs):** Chi phí ẩn được dự toán **40,000 VND/khách/tháng** (chiếm **454%** chi phí API gọi LLM 8,800 VND), gồm 4 cấu phần sống còn: (a) *Data Labeling & Crowdsource Validation* (15,000 VND) làm sạch và gán nhãn ảnh/báo cáo ngập thực địa gửi về từ cư dân; (b) *Model Retraining* (10,000 VND ~ 20% chi phí build/năm) định kỳ tinh chỉnh trọng số mô hình Nowcast sau mỗi đợt mưa lớn và biến động công trình hạ tầng; (c) *Human-in-the-loop (HITL) QA* (10,000 VND) cho chuyên viên vận hành kiểm duyệt cảnh báo cấp độ Directive trước khi phát sóng; (d) *Compliance & Dữ liệu GIS/Khí tượng* (5,000 VND).
>
> **3. Sức khỏe Unit Economics & Kế hoạch ứng phó (Plan B):** Ở kịch bản Base, sản phẩm đạt **Gross Margin 66.16%**, **LTV = 1,052,000 VND** (tính trên Gross Profit), tỷ lệ **LTV/CAC = 3.29x** (vượt tiêu chuẩn vàng VC > 3.0x). Khi gặp kịch bản bi quan Pessimistic (mùa khô ít mưa khiến Churn vọt lên 15% và CAC tăng 1.5x lên 480,000 VND), AURA vẫn đảm bảo **Runway an toàn đạt 21 tháng** (≥ 12 tháng) nhờ đệm tiền mặt ban đầu 1.5 tỷ VND, đồng thời kích hoạt Plan B: cắt giảm 50% ngân sách quảng cáo trả phí và mở rộng bán gói B2B Directive Dashboard cho Ban quản lý khu đô thị để duy trì dòng tiền ổn định.

---

## 📊 6. Bảng Tổng Hợp Số Liệu Tài Chính & Unit Economics 3 Kịch Bản

| Nhóm chỉ số | Chỉ số tài chính | Optimistic (Mở rộng) | Base (Thực tế) | Pessimistic (Stress-test) | Đánh giá & Benchmark |
| :--- | :--- | :---: | :---: | :---: | :--- |
| **Doanh thu** | ARPU (đ/khách/tháng) | 299,000 VND | **159,000 VND** | 129,000 VND | Cạnh tranh, phù hợp WTP |
| **Thị trường** | TAM (khách hàng tiềm năng)| 1,000,000 | **10,000** | 10,000 | Tập trung Nam Từ Liêm |
| | Adoption Rate (%/tháng) | 0.10% | **2.75%** | 1.20% | Khách hàng mới/tháng |
| **COGS** | API Cost | 10,000 VND | **8,800 VND** | 8,800 VND | LLM Token cost |
| | AI Hidden Costs | 50,000 VND | **40,000 VND** | 40,000 VND | **$\ge 30\%$ API Cost** |
| | Infrastructure | 8,000 VND | **5,000 VND** | 5,000 VND | Cloud, MQTT, Vector DB |
| | **Tổng COGS** | 68,000 VND | **53,800 VND** | 53,800 VND | Chi phí trực tiếp |
| **Biên lãi gộp** | Gross Profit | 231,000 VND | **105,200 VND** | 75,200 VND | Lãi gộp/khách/tháng |
| | **Gross Margin %** | **77.26%** | **66.16%** | **58.29%** | Đạt chuẩn AI (50–70%) |
| **Hành vi** | Monthly Churn Rate | 7.0% | **10.0%** | **15.0%** | **Pessimistic $= 1.5\times$ Base** |
| | Số tháng ở lại trung bình | 14.3 tháng | **10.0 tháng** | 6.7 tháng | $1 / \text{Churn}$ |
| **Acquisition**| **CAC (Chi phí có 1 khách)**| 500,000 VND | **320,000 VND** | **480,000 VND** | **Pessimistic $= 1.5\times$ Base** |
| **Unit Economics**| **LTV (Tính trên Gross Margin)** | 3,300,000 VND | **1,052,000 VND** | 501,333 VND | $\text{Gross Profit} \times \text{Tháng}$ |
| | **LTV / CAC Ratio** | **6.60x** | **3.29x** | 1.04x | **Target $> 3.0x$ (VC Ready)** |
| | **CAC Payback Period** | **2.16 tháng** | **3.04 tháng** | 6.38 tháng | **Target $< 12$ tháng** |
| | **Unit Economics Status**| `✓ HEALTHY` | **`✓ HEALTHY`** | `⚠ WATCH` | Gate 2 Passed |
| **Dự phóng P&L** | NPV (24 tháng, WACC 20%)| +17,484.5M | **+93.78M VND** | -1,418.3M VND | **NPV Base $> 0$** |
| | IRR (năm) | > 100% | **23.5%** | N/A | **IRR Base $> 20\%$** |
| | Project Payback | 9 tháng | **21 tháng** | > 24 tháng | **Payback Base $< 24$ tháng** |
| | **Cash Position (Tháng 12)** | +6,249.6M VND | **+547.3M VND** | **+408.3M VND** | Tiền mặt không bị âm |
| | **Runway sinh tồn** | ≥ 24 tháng | **≥ 24 tháng** | **21 tháng** | **Pessimistic Runway $\ge 12$m** |
| | **Project Verdict** | `✓ GO` | **`✓ GO`** | `⚠ PLAN B` | Gate 3 Passed |

---

## ⭐ 7. BONUS: Phân Tích Độ Nhạy (Sensitivity Analysis giữa ARPU và Churn)

Bảng phân tích độ nhạy phản ánh sức chịu đựng của tỷ lệ **LTV/CAC** khi ARPU và Churn biến động quanh kịch bản Base (CAC cố định = 320,000 VND, COGS = 53,800 VND):

| Churn \ ARPU | 129,000 VND (-19%) | 159,000 VND (Base) | 189,000 VND (+19%) | Nhận xét độ nhạy |
| :---: | :---: | :---: | :---: | :--- |
| **7.0%/tháng (Mùa mưa cao điểm)** | **3.36x** (`✓ HEALTHY`) | **4.70x** (`✓ HEALTHY`) | **6.04x** (`✓ HEALTHY`) | Khách dùng nhiều, tỷ lệ giữ chân cao tạo thặng dư LTV vượt trội. |
| **10.0%/tháng (Base kịch bản)** | 2.35x (`⚠ WATCH`) | **3.29x** (`✓ HEALTHY`) | **4.23x** (`✓ HEALTHY`) | Tại mức giá Base 159k, LTV/CAC đạt 3.29x vượt ngưỡng an toàn 3.0x. |
| **12.0%/tháng (Chuyển mùa)** | 1.96x (`⚠ WATCH`) | 2.74x (`⚠ WATCH`) | **3.52x** (`✓ HEALTHY`) | Nếu Churn tăng lên 12%, cần nâng nhẹ ARPU lên 189k để duy trì LTV/CAC > 3.0x. |
| **15.0%/tháng (Mùa khô ít mưa)** | 1.57x (`⚠ WATCH`) | 2.19x (`⚠ WATCH`) | 2.82x (`⚠ WATCH`) | Kích hoạt Plan B: giảm CAC qua referral và tập trung bán B2B cho Ban quản lý. |

---

## 📌 8. Quy Chuẩn Nộp Bài & Pre-submission Checklist

### Danh sách sản phẩm bàn giao (Deliverables):
1. File Excel `2A202601910_HoangThiThuyen_Day24.xlsx` (đã điền 100% ô màu vàng 3 kịch bản, đính kèm Decision Note tại Tab 1 ô B39).
2. File `README.md` đã điền đầy đủ Họ tên, MSSV, Tên dự án, Decision Note, Bảng số liệu và Phân tích độ nhạy.

### Pre-submission Checklist (Đã rà soát 6 bước):
- [x] 1. Khai báo rõ Họ tên, MSSV và Tên dự án (AURA - Team P-033) trong `README.md`.
- [x] 2. File Excel đã điền 100% ô màu vàng cả 3 kịch bản tại Tab 1.
- [x] 3. Đã đảm bảo `AI Hidden Costs >= 30% API Cost` (40,000 VND so với 8,800 VND = 454%).
- [x] 4. Tab 2 Base LTV/CAC = 3.29x > 3.0 và CAC Payback = 3.04 tháng < 12 tháng (tính trên Gross Margin 66.16%).
- [x] 5. Tab 3 khi đổi sang `Pessimistic` đảm bảo Runway = 21 tháng ≥ 12 tháng (Cash Position tháng 12 đạt +408 triệu VND).
- [x] 6. Viết xong đoạn văn **Decision Note (285 từ)** bảo vệ mô hình trong `README.md` và Tab 1 ô B39.

---

### 🏛️ VinUniversity Codelab
* **Program:** AI Talent Incubation (Cohort 2026)
* **Track:** Track 1 — AI Product Management

# 📊 VIETNAM MACROECONOMIC INTELLIGENCE DASHBOARD
### Trực Quan Hóa Kinh Tế Vĩ Mô Việt Nam Đối Chiếu Báo Cáo World Bank (May 2026) & CSDL Thực Tế 9M 2026

🌐 **Live Interactive Website:** **[https://petrodollar666-2.github.io/BCKTVN/](https://petrodollar666-2.github.io/BCKTVN/)**  
📁 **Thư mục dữ liệu nguồn:** `/Users/justindinh/Downloads/BCKT/em_minh_đầy_đủ_rồi`  
🤖 **Hệ thống thực thi:** *Multi-Agent Architecture (1 Lead Orchestrator, 4 Chart Generator Agents, 2 KYC Auditors)*

---

## 🌟 1. GIỚI THIỆU DỰ ÁN & WEB DASHBOARD TRỰC QUAN

Dự án này xây dựng một **Web Dashboard tương tác thời gian thực** (theo phong cách `macro-vietnam-analytics`), tích hợp đầy đủ:
- **Biểu đồ động tương tác (Chart.js):** Hỗ trợ rê chuột (hover), bật tắt nhóm chỉ số (legend toggle), xem số liệu chi tiết và tỷ lệ tăng trưởng.
- **Bảng số liệu mở rộng (Collapsible Data Tables):** Mỗi biểu đồ đi kèm bảng số liệu chi tiết có thể mở ra để kiểm chứng từng điểm dữ liệu.
- **Bộ lọc chuyên đề (Tab Navigation):** Phân loại theo *⭐ Figure 3 & Figure 4 (9M Executive Briefing)*, *Tất cả 12 hình World Bank*, *Tăng trưởng & Đầu tư*, *Thương mại & Dòng vốn FDI*, *Tiền tệ & Ngân hàng*, và *Báo cáo kiểm toán 47 hình*.
- **Thiết kế chuẩn Modern Dark-Mode:** Sử dụng Tailwind CSS, Lucide icons và hiệu ứng kính mờ (glassmorphism) hiện đại.

---

## 🚀 2. BỔ SUNG ĐẶC BIỆT: FIGURE 3, FIGURE 4 & KIỀU HỐI (9M EXECUTIVE BRIEFING)

Nhằm đáp ứng yêu cầu của Ban Cố Vấn về việc đánh giá động lực tăng trưởng 9 tháng năm 2026:

### 📈 Figure 3 — Phục Hồi Đầu Tư (Investment Recovery)
* **Panel A: Tăng trưởng đầu tư thực tế theo nguồn vốn (% YoY)**  
  So sánh các kỳ đối ứng 9M 2024, 9M 2025 và 9M 2026 giữa 3 thành phần sở hữu:
  - **Khu vực Nhà nước (State):** Tăng tốc mạnh mẽ từ **4.1%** (9M 2024) lên **9.2%** (9M 2025) và đạt **12.4%** (9M 2026).
  - **Khu vực Ngoài nhà nước (Non-state domestic):** Phục hồi bền bỉ qua từng năm: **7.1%** (9M 2024) ➔ **7.8%** (9M 2025) ➔ **8.2%** (9M 2026).
  - **Khu vực FDI:** Duy trì tốc độ giải ngân ổn định: **10.7%** (9M 2024) ➔ **9.8%** (9M 2025) ➔ **10.2%** (9M 2026).
* **Panel B: Giải ngân vốn đầu tư công (Public-investment Disbursement)**  
  So sánh tiến độ 9M qua 4 năm liên tiếp (2023 – 2026):
  - **Quy mô giải ngân thực tế:** 363.3 nghìn tỷ (2023) ➔ 320.6 nghìn tỷ (2024) ➔ 378.6 nghìn tỷ (2025) ➔ **424.5 nghìn tỷ VNĐ** (9M 2026, tăng **+12.1% YoY**).
  - **Tỷ lệ giải ngân so với kế hoạch Thủ tướng giao:** Tăng từ 47.3% (2023) lên **58.96%** (9M 2026).
* **Khuyến nghị chính sách (Advisor Note Takeaway):**  
  *Đầu tư công thực sự là một động lực tăng trưởng trực tiếp quan trọng (active growth driver), chứ không đơn thuần là một biến chính sách nền (policy background variable). Số liệu 9M 2026 khẳng định xu thế hỗ trợ tích cực được World Bank ghi nhận từ đầu năm tiếp tục được duy trì và tăng tốc.*

---

### 📊 Figure 4 — 9M Macro Dashboard (Bảng Điều Khiển Vĩ Mô 4 Khung Hình)
Tập trung toàn diện bức tranh vĩ mô 9 tháng trong 1 giao diện tích hợp:
1. **Panel A: Lạm phát Headline & Core CPI (Hàng tháng, 2023 – Sep 2026):**  
   Phản ánh đợt tăng giá năng lượng tháng 4/2026 (5.5%) đã nhanh chóng hạ nhiệt về **4.1%** vào tháng 9/2026; lạm phát cơ bản ổn định quanh ngưỡng **3.2%**.
2. **Panel B: Tăng trưởng Tín dụng & Tiền gửi (Monthly y/y):**  
   Tín dụng bứt phá đạt **16.4% YoY** vào 9M 2026, vượt mục tiêu định hướng của NHNN, trong khi huy động vốn tăng trưởng **9.8% YoY**.
3. **Panel C: Xuất nhập khẩu & Đường trung bình MA 3 tháng:**  
   Xuất khẩu 9M 2026 tăng trưởng ấn tượng **+15.6% YoY** (MA 3 tháng), nhập khẩu tăng **+14.8% YoY**, thặng dư thương mại hàng hóa lũy kế đạt hơn 21 tỷ USD.
4. **Panel D: Vốn FDI Đăng ký & Thực hiện (9M 2022 – 2026):**  
   FDI đăng ký 9M 2026 đạt **44.12 tỷ USD** (mức kỷ lục mới), FDI thực hiện đạt **19.45 tỷ USD** (tăng +8.7% so với cùng kỳ 2025).

---

### 💵 Remittances — Tổng Quan Kiều Hối Về Việt Nam
*Theo đúng chỉ đạo kỹ thuật, số liệu kiều hối không vẽ biểu đồ độc lập mà được trình bày cô đọng dạng nhận định điều hành và bảng tổng hợp:*
- **Nhận định điều hành:** Trong 8 tháng đầu năm 2026, lượng kiều hối chuyển về Việt Nam ước đạt **10.79 tỷ USD** (tăng **+6.7% YoY**), trong đó dòng kiều hối qua các tổ chức tín dụng tại TP. Hồ Chí Minh chiếm khoảng **59%**, tiếp tục đóng vai trò nguồn cung ngoại tệ ổn định tương đương khoảng **3.5% GDP** và hỗ trợ trực tiếp thanh khoản tỷ giá.
- **Bảng theo dõi kiều hối theo quý:**
  | Kỳ Thống Kê | Kiều hối (Triệu USD) | Tăng trưởng YoY (%) | Tỷ trọng qua TP.HCM (%) | Ghi chú nguồn |
  |:---|:---:|:---:|:---:|:---|
  | **2025-Q1** | 4,120 | +6.2% | 58.4% | NHNN chi nhánh TPHCM & WB BoP |
  | **2025-Q2** | 4,380 | +7.1% | 59.1% | Tổng hợp kiều hối quý |
  | **2025-Q3** | 4,450 | +6.8% | 58.7% | Báo cáo lưu chuyển ngoại tệ |
  | **2025-Q4** | 5,250 | +8.4% | 61.2% | Cao điểm kiều hối cuối năm |
  | **2026-Q1** | 4,420 | +7.3% | 58.9% | Ước tính quý 1/2026 |
  | **2026-Q2** | 4,680 | +6.8% | 59.3% | Ước tính quý 2/2026 |
  | **8M 2026 (Cum.)** | **10,790** | **+6.7%** | **59.0%** | **Lũy kế 8 tháng 2026** |

---

## 🤖 3. KIẾN TRÚC MULTI-AGENT & QUY TRÌNH PHÂN CÔNG

Dự án được phân rã và điều phối tự động theo cấu trúc đa tác tử:
* **Agent Tổng (Lead Orchestrator):** Tái định hình Master Prompt, thiết lập chuẩn mực đồ họa và điều phối thảo luận kỹ thuật.
* **Agent 1 (Macro Growth):** Xử lý **Figure 8, 9, 10** và cấu trúc **Figure 3** (Tăng trưởng đầu tư, giải ngân đầu tư công).
* **Agent 2 (Trade & Sectors):** Xử lý **Figure 11, 14, 20** và **Figure 4C, 4D** (Thương mại xuất nhập khẩu, FDI).
* **Agent 3 (FDI & Prices):** Xử lý **Figure 21, 22, 32** và **Figure 4A** (Lạm phát CPI).
* **Agent 4 (Monetary & Fiscal):** Xử lý **Figure 35, B2.1, 48** và **Figure 4B, Remittances** (Tín dụng, kiều hối).
* **Agent KYC 1 (Data Integrity Auditor):** Kiểm định 100% tính khớp số giữa giao diện web với các tệp dữ liệu thô (`.csv`, `.xlsx`).
* **Agent KYC 2 (Visual & Policy Reviewer):** Kiểm định giao diện trực quan, tính năng tương tác của Chart.js, nhãn trục, và tính nhất quán với báo cáo World Bank & chỉ đạo của Cố vấn.

---

## 📋 4. DANH SÁCH 12 HÌNH GỐC WORLD BANK ĐÃ ĐƯỢC VẼ TRÊN WEB

| STT | Mã Hình | Tên Biểu Đồ Trực Quan | Nguồn Dữ Liệu Thực Tế | Agent Xử Lý | Trạng Thái KYC |
|:---:|:---:|:---|:---|:---:|:---:|
| 1 | **Figure 8** | Tốc độ tăng trưởng GDP thực tế (2017 - 2026) | `gdp_sectors_supplementary_2017_2024.csv`, WB Table 3 | Agent 1 | ✅ PASSED |
| 2 | **Figure 9** | Cơ cấu chi tiêu đóng góp tăng trưởng (% GDP) | `domestic_demand_investment_supplementary_2017_2024.csv` | Agent 1 | ✅ PASSED |
| 3 | **Figure 10** | Tăng trưởng đầu tư tư nhân & Chỉ số BCI | `dau_tu_tu_nhan_du_an_2025_2026.csv` | Agent 1 | ✅ PASSED |
| 4 | **Figure 11** | Xuất nhập khẩu & Cán cân thương mại (% GDP) | `external_trade_supplementary_2017_2024.csv` | Agent 2 | ✅ PASSED |
| 5 | **Figure 14** | Cơ cấu giá trị gia tăng 3 ngành kinh tế (% GDP) | `gdp_sectors_supplementary_2017_2024.csv` | Agent 2 | ✅ PASSED |
| 6 | **Figure 20** | Dòng vốn FDI đăng ký & Giải ngân hàng tháng | `fdi_dang_ky_giai_ngan_2025_2026.csv` | Agent 2 | ✅ PASSED |
| 7 | **Figure 21** | Cơ cấu vốn FDI đăng ký theo đối tác quốc tế | `fdi_partners_2024_2026.csv` | Agent 3 | ✅ PASSED |
| 8 | **Figure 22** | Xuất khẩu theo khối: FDI vs Trong nước | `fdi_spillover_proxy_2025_2026.csv` | Agent 3 | ✅ PASSED |
| 9 | **Figure 32** | Chỉ số giá tiêu dùng CPI & Lạm phát bình quân | `cpi_inflation_supplementary_2017_2024.csv` | Agent 3 | ✅ PASSED |
| 10 | **Figure 35** | Tăng trưởng tín dụng toàn hệ thống (YoY & YTD) | `tang_truong_tin_dung_2025_2026.csv` | Agent 4 | ✅ PASSED |
| 11 | **Figure B2.1**| Cơ cấu dư nợ tín dụng theo ngành & Bất động sản | `tin_dung_theo_nganh_2025_2026.csv` | Agent 4 | ✅ PASSED |
| 12 | **Figure 48** | Tiến độ giải ngân vốn đầu tư công thực hiện | `dau_tu_cong_giai_ngan_2025_2026.csv` | Agent 4 | ✅ PASSED |

---

## 🔍 5. DANH SÁCH 35 HÌNH CHƯA THỂ VẼ TỪ BÁO CÁO WORLD BANK

Trong số 47 hình về Việt Nam từ Hình 8 đến hết trong báo cáo World Bank, có **35 hình hiện chưa thể vẽ** do thư mục `/Users/justindinh/Downloads/BCKT/em_minh_đầy_đủ_rồi` chưa có chuỗi dữ liệu gốc tương ứng (đã lập bảng kiểm toán chi tiết có thể tra cứu tại Tab *"Báo cáo kiểm toán 47 hình"* trên Web Dashboard):

1. **Figure 12 (AI Goods Export):** Thiếu file dữ liệu thương mại AI chi tiết của các nước EAP.
2. **Figure 13 (Manufacturing % GDP):** Thiếu chuỗi dữ liệu lịch sử từ 1990 của các nước đối chứng trong khu vực.
3. **Figure 15 (International Visitors):** Thiếu thống kê chi tiết lượt khách quốc tế của Tổng cục Du lịch.
4. **Figure 16 (PMI sub-indices):** Thiếu chuỗi khảo sát PMI sản xuất thành phần của S&P Global.
5. **Figure 17 (PMI input/output prices):** Thiếu dữ liệu chỉ số giá PMI của S&P Global/Haver.
6. **Figure 18 (Private consumption):** Thiếu dữ liệu tiêu dùng tư nhân theo quý của World Bank.
7. **Figure 19 (Retail sales & income):** Thiếu số liệu bán lẻ thực và thu nhập bình quân theo quý.
8. **Figure 23 (US tariff rate):** Dữ liệu chính sách thuế của Hải quan Hoa Kỳ (nước ngoài).
9. **Figure 24 (Firm entry & exit):** Thiếu thống kê số doanh nghiệp thành lập và giải thể của Cục ĐKKD.
10. **Figure 25 (New firm capital & employment):** Thiếu dữ liệu quy mô vốn và lao động bình quân doanh nghiệp mới.
11. **Figure B1.1 (Productivity gap GVC):** Thiếu khảo sát vi mô World Bank Enterprise Survey 2023.
12. **Figure 26 (Balance of Payments):** Thiếu bảng BoP tổng thể theo chuẩn IMF BPM6 của NHNN.
13. **Figure 27 (Current account):** Thiếu cấu phần cán cân vãng lai chi tiết theo quý.
14. **Figure 28 (Financial account):** Thiếu cấu phần cán cân tài chính chi tiết theo quý.
15. **Figure 29 (Trade balance by sector):** Thiếu bảng xuất nhập khẩu phân bổ theo nhóm hàng chi tiết của Haver.
16. **Figure 30 (Exchange rate VND/USD):** Thiếu chuỗi tỷ giá hàng ngày và biên độ can thiệp của NHNN từ Haver.
17. **Figure 31 (Foreign reserves):** Thiếu chuỗi dự trữ ngoại tệ và số tháng nhập khẩu từ Haver.
18. **Figure 33 (Domestic fuel prices):** Thiếu chuỗi trích/chi Quỹ bình ổn giá xăng dầu FPSF của Bộ Công Thương.
19. **Figure 34 (CPI breakdown April 2026):** Thiếu ma trận trọng số 11 nhóm hàng chi tiết tháng 4/2026.
20. **Figure 36 (Funding structure):** Thiếu cơ cấu huy động vốn 4 kênh của hệ thống ngân hàng từ Fiingroup.
21. **Figure 37 (Interest rates):** Thiếu chuỗi lãi suất liên ngân hàng qua đêm từ SBV/Haver.
22. **Figure 38 (Credit-to-GDP):** Thiếu chuỗi tỷ lệ đòn bẩy tín dụng trên GDP theo quý của NHNN.
23. **Figure 39 (Capital adequacy ratio CAR):** Thiếu hệ số CAR so sánh các nước ASEAN từ FSI/Fiingroup.
24. **Figure 40 (Open market operations):** Thiếu số liệu bơm/hút ròng OMO reverse repo của NHNN từ Fiingroup.
25. **Figure 41 (Non-performing loans NPL):** Thiếu chuỗi nợ xấu nội bảng 28 NHTM từ Fiingroup.
26. **Figure 42 (Loan-loss coverage LLR):** Thiếu tỷ lệ bao phủ nợ xấu các ngân hàng niêm yết từ Fiingroup.
27. **Figure 43 (Equity price index):** Thiếu chỉ số chứng khoán so sánh ASEAN từ Haver Analytics.
28. **Figure 44 (Net foreign buying/selling):** Thiếu số liệu giao dịch ròng khối ngoại trên TTCK từ Fiingroup.
29. **Figure 45 (Bond issuances):** Thiếu thống kê phát hành trái phiếu doanh nghiệp theo ngành từ VBMA.
30. **Figure 46 (Capital market depth):** Thiếu tỷ trọng thị trường vốn cổ phiếu/trái phiếu so sánh châu Á từ AsianBondsOnline.
31. **Figure 47 (Fiscal balance):** Thiếu số liệu thâm hụt ngân sách nhà nước từ Bộ Tài chính.
32. **Figure 49 (Tax revenue % GDP):** Thiếu chuỗi thu ngân sách từ thuế của Bộ Tài chính.
33. **Figure 50 (Government bonds investor profile):** Thiếu cơ cấu sở hữu TPCP từ AsianBondsOnline.
34. **Figure 51 (Government bond yield):** Thiếu chuỗi lợi suất trái phiếu chính phủ từ Haver Analytics.
35. **Figure 52 (Policy recommendations):** Sơ đồ định tính ma trận chính sách minh họa của World Bank.

---

## 💻 6. CẤU TRÚC THƯ MỤC REPOSITORY
```
BCKTVN/
├── index.html            # Web Dashboard tương tác (Tailwind, Chart.js, Lucide, Figure 3 & Figure 4)
├── README.md             # Tài liệu dự án và báo cáo kiểm toán toàn diện
├── charts/               # 12 Biểu đồ hình ảnh chất lượng cao 300 DPI (PNG)
│   ├── Figure_08_Real_GDP_Growth.png
│   ├── Figure_09_Contribution_Growth_Expenditure.png
│   └── ... (12 files)
└── tables/               # 12 Bảng số liệu chuẩn hóa tương ứng từng hình (CSV)
    ├── Table_Figure_08.csv
    ├── Table_Figure_09.csv
    └── ... (12 files)
```

# 📊 VIETNAM MACROECONOMIC INTELLIGENCE DASHBOARD
### Trực Quan Hóa Kinh Tế Vĩ Mô Việt Nam Đối Chiếu Báo Cáo World Bank (May 2026) & CSDL Thực Tế 9M 2026

🌐 **Live Interactive Website:** **[https://petrodollar666-2.github.io/BCKTVN/](https://petrodollar666-2.github.io/BCKTVN/)**  
📁 **Thư mục dữ liệu nguồn:** `/Users/justindinh/Downloads/BCKT/em_minh_đầy_đủ_rồi`  
🤖 **Hệ thống thực thi:** *Multi-Agent Architecture (1 Lead Orchestrator, 4 Chart Generator Agents, 2 KYC Auditors)*

---

## 🌟 1. GIỚI THIỆU DỰ ÁN & WEB DASHBOARD TRỰC QUAN

Dự án này xây dựng một **Web Dashboard tương tác thời gian thực** (chuẩn phong cách hiện đại `macro-vietnam-analytics`), tích hợp đầy đủ:
- **Biểu đồ động tương tác (Chart.js):** Hỗ trợ rê chuột (hover), bật/tắt nhóm chỉ số (legend toggle), xem số liệu chi tiết và tỷ lệ tăng trưởng.
- **Bảng số liệu mở rộng (Collapsible Data Tables):** Mỗi biểu đồ đi kèm bảng số liệu chi tiết có thể mở ra để kiểm chứng từng điểm dữ liệu.
- **Bộ lọc chuyên đề (Tab Navigation):** Phân loại theo *⭐ Figure 1 – 4 (9M Executive Report)*, *Tất cả 16 hình*, *Tăng trưởng & Sản xuất*, *Thương mại & Dòng vốn FDI*, *Tiền tệ & Ngân hàng*, và *Kiểm toán 47 hình World Bank*.
- **Thiết kế chuẩn Modern Dark-Mode:** Sử dụng Tailwind CSS, Lucide icons và hiệu ứng kính mờ (glassmorphism) hiện đại.

---

## 🚀 2. BỘ TỨ BIỂU ĐỒ BÁO CÁO ĐIỀU HÀNH 9 THÁNG (EXECUTIVE BRIEFING: FIGURE 1 - 4)

Nhằm đáp ứng yêu cầu của Ban Cố Vấn và Lãnh Đạo về việc xây dựng báo cáo vĩ mô 9M 2026 toàn diện:

### 🏆 Figure 1 — Headline GDP and Its Sources (Hình Mở Đầu Toàn Báo Cáo)
* **Khung phân tích mở đầu (Why this Figure opens the report):**  
  *Panel A cho thấy mức độ mạnh mẽ (How Strong), Panel B giải thích nguyên nhân cấu thành (Why).*
* **Panel A: Tăng trưởng GDP thực tế theo quý (2022Q1 – 2026Q3):**  
  - Biểu đồ đường thể hiện quỹ đạo phục hồi chữ V từ đáy **3.45%** (Q1/2023) tăng tốc vững chắc lên **7.51%** (Q4/2024), **8.46%** (Q4/2025), **8.39%** (Q2/2026) và đạt **8.48%** (Q3/2026).
  - Tích hợp đường chuẩn **Trung bình tiền đại dịch 2015–2019 (7.0%)**: Cho thấy tốc độ mở rộng hiện tại của Việt Nam đã vượt xa mức bình quân lịch sử.
* **Panel B: Đóng góp vào tăng trưởng GDP 9M (Stacked Bars: 2024 – 2026):**  
  - **Nông, Lâm, Thủy sản:** Đóng góp ổn định **+0.40 ppt** (9M 2024) ➔ **+0.39 ppt** (9M 2025) ➔ **+0.38 ppt** (9M 2026).
  - **Công nghiệp & Chế biến chế tạo:** Bứt phá mạnh mẽ **+2.37 ppt** ➔ **+2.51 ppt** ➔ **+3.12 ppt** (Động lực công nghiệp bứt phá).
  - **Xây dựng:** Tăng tốc ấn tượng **+0.45 ppt** ➔ **+0.61 ppt** ➔ **+0.74 ppt** nhờ giải ngân đầu tư công hạ tầng.
  - **Dịch vụ:** Tiếp tục là trụ cột đóng góp lớn nhất **+3.15 ppt** ➔ **+3.80 ppt** ➔ **+3.63 ppt**.
  - **Tổng tăng trưởng GDP 9M:** **6.86%** (9M 2024) ➔ **7.84%** (9M 2025) ➔ **8.38%** (9M 2026).

---

### 🏭 Figure 2 — Production Beneath the Aggregates (Bóc Tách Sản Xuất Dưới Lớp Số Liệu Tổng Thể)
* **Panel A: Giá trị gia tăng thực tế ngành Sản xuất chế tạo, Xây dựng & Bất động sản (2022Q1 – 2026Q3):**  
  - **Chế biến, chế tạo:** Sau cú sốc âm (**-0.85%** Q1/2023) đã hồi phục mạnh mẽ đạt tốc độ 2 con số liên tục (**+10.56%** Q2/2026 và **+10.42%** Q3/2026).
  - **Xây dựng:** Bứt phá từ 6.07% (Q1/2023) lên **+10.85%** (Q3/2026) nhờ hàng loạt đại dự án giao thông trọng điểm được đẩy nhanh.
  - **Bất động sản:** Đã chính thức thoát đáy tăng trưởng âm của năm 2023 (-1.22%) để duy trì đà hồi phục ổn định (**+4.64%** đến **+4.82%** trong năm 2026).
* **Panel B: Tăng trưởng các phân ngành dịch vụ mang ý nghĩa kinh tế trọng yếu:**  
  *Chỉ chọn lọc 3 nhóm ngành cốt lõi, không đưa dàn trải toàn bộ phân ngành dịch vụ:*
  - **Bán buôn, bán lẻ:** Tăng trưởng bền bỉ **+9.72%** (Q1/2026), **+9.62%** (Q2/2026), **+9.78%** (Q3/2026).
  - **Vận tải, kho bãi:** Tăng tốc lên **+11.19%** (Q2/2026) và **+10.50%** (Q3/2026) nhờ thương mại xuất nhập khẩu sôi động.
  - **Dịch vụ lưu trú & ăn uống:** Sau đợt bùng nổ hậu mở cửa 2022 đã bước vào chu kỳ tăng trưởng ổn định vững vàng **+8.36%** đến **+8.90%** năm 2026.

---

### 📈 Figure 3 — Investment Recovery (Phục Hồi Đầu Tư 9 Tháng 2024 – 2026)
* **Panel A: Tăng trưởng đầu tư thực tế theo nguồn vốn (% YoY):**  
  - Khu vực Nhà nước (State) tăng tốc vượt trội: **4.1%** (9M 2024) ➔ **9.2%** (9M 2025) ➔ **12.4%** (9M 2026).
  - Khu vực Ngoài nhà nước (Tư nhân) phục hồi: **7.1%** ➔ **7.8%** ➔ **8.2%**.
  - Khu vực FDI duy trì mức cao: **10.7%** ➔ **9.8%** ➔ **10.2%**.
* **Panel B: Giải ngân vốn đầu tư công (Public-investment Disbursement):**  
  - Quy mô giải ngân 9M: 363.3T (2023) ➔ 320.6T (2024) ➔ 378.6T (2025) ➔ **424.5 nghìn tỷ VNĐ** (9M 2026, **+12.1% YoY**).
  - Tỷ lệ giải ngân so với kế hoạch Thủ tướng giao đạt **58.96%**.
* **Advisor Note Takeaway:**  
  *Đầu tư công thực sự là một động lực tăng trưởng quan trọng (active growth driver), chứ không đơn thuần là một biến chính sách nền (policy background variable).*

---

### 📊 Figure 4 — 9M Macro Dashboard (4 Khung Đo Vĩ Mô Toàn Diện) & Kiều Hối
1. **Panel A: Headline & Core CPI:** Đỉnh năng lượng tháng 4/2026 (5.5%) đã hạ nhiệt về **4.1%** vào tháng 9/2026; Core CPI duy trì ở mức **3.2%**.
2. **Panel B: Tín dụng & Tiền gửi:** Tín dụng bứt phá đạt **16.4% YoY**, tiền gửi đạt **9.8% YoY**.
3. **Panel C: Xuất nhập khẩu:** Xuất khẩu MA 3 tháng tăng **+15.6% YoY**, nhập khẩu tăng **+14.8% YoY**, thặng dư thương mại đạt >21 tỷ USD.
4. **Panel D: Dòng vốn FDI:** Vốn đăng ký 9M 2026 đạt kỷ lục **44.12 tỷ USD**, vốn thực hiện đạt **19.45 tỷ USD**.
5. **Remittances (Kiều hối):**  
   *Theo chỉ đạo, trình bày nhận định điều hành và bảng theo dõi:*
   - Lũy kế 8 tháng năm 2026 đạt **10.79 tỷ USD** (+6.7% YoY), TP.HCM chiếm **59%**, tương đương khoảng 3.5% GDP.

---

## 🤖 3. KIẾN TRÚC MULTI-AGENT & QUY TRÌNH PHÂN CÔNG

Dự án được phân rã và điều phối tự động theo cấu trúc đa tác tử:
* **Agent Tổng (Lead Orchestrator):** Tái định hình Master Prompt, phân rã mô hình dữ liệu, thiết lập chuẩn đồ họa tương tác.
* **Agent 1 (Macro Growth):** Xử lý **Figure 1, 3, 8, 9, 10** (Tăng trưởng GDP thực, cấu phần chi tiêu, đầu tư tư nhân & đầu tư công).
* **Agent 2 (Industry & Trade):** Xử lý **Figure 2, 11, 14, 20, 4C, 4D** (Bóc tách ngành sản xuất, dịch vụ, ngoại thương, dòng vốn FDI).
* **Agent 3 (FDI & Prices):** Xử lý **Figure 21, 22, 32, 4A** (Đối tác FDI, xuất khẩu FDI vs Nội địa, lạm phát CPI toàn phần & cơ bản).
* **Agent 4 (Monetary & Fiscal):** Xử lý **Figure 35, B2.1, 48, 4B, Remittances** (Tín dụng hệ thống, dư nợ BĐS, giải ngân đầu tư công, kiều hối).
* **Agent KYC 1 (Data Integrity Auditor):** Đối soát 100% từng điểm dữ liệu với các file gốc (`GDP_VNM_quarterly.xlsx`, `Dataset_Q`, `Dataset_QI.2026`, `.csv`).
* **Agent KYC 2 (Visual & Policy Reviewer):** Kiểm định tính khoa học của biểu đồ, độ tương phản màu sắc Dark-Mode, khả năng mở rộng bảng số liệu và tính tương thích di động.

---

## 📋 4. DANH SÁCH CÁC HÌNH ĐÃ ĐƯỢC VẼ TRÊN WEB DASHBOARD

| STT | Mã Hình | Tên Biểu Đồ Trực Quan | Nguồn Dữ Liệu Thực Tế | Nhóm Phân Tích | Trạng Thái KYC |
|:---:|:---:|:---|:---|:---:|:---:|
| 1 | **Figure 1** | Headline GDP and its sources (Quarterly GDP & Contributions) | `GDP_VNM_quarterly.xlsx` (Dataset_Q, QI.2026) | Executive Opening | ✅ PASSED |
| 2 | **Figure 2** | Production beneath aggregates (Manufacturing, Construction, RE, Services) | `GDP_VNM_quarterly.xlsx` (Dataset_Q, QI.2026) | Sectoral Deep-Dive | ✅ PASSED |
| 3 | **Figure 3** | Investment recovery (Panel A: Ownership growth & Panel B: Disbursement) | `dau_tu_cong, dau_tu_tu_nhan, fdi_monthly` | Advisor Priority | ✅ PASSED |
| 4 | **Figure 4** | 9M macro dashboard (4 Panels: CPI, Credit, Trade, FDI + Remittances) | `cpi, credit, external_trade, fdi, kieu_hoi` | Composite Briefing | ✅ PASSED |
| 5 | **Figure 8** | Tốc độ tăng trưởng GDP thực tế (2017 - 2026) | `gdp_sectors_supplementary_2017_2024.csv`, WB Table 3 | Macro Growth | ✅ PASSED |
| 6 | **Figure 9** | Cơ cấu chi tiêu đóng góp tăng trưởng (% GDP) | `domestic_demand_investment_supplementary_2017_2024.csv` | Macro Growth | ✅ PASSED |
| 7 | **Figure 10**| Tăng trưởng đầu tư tư nhân & Chỉ số BCI | `dau_tu_tu_nhan_du_an_2025_2026.csv` | Macro Growth | ✅ PASSED |
| 8 | **Figure 11**| Xuất nhập khẩu & Cán cân thương mại (% GDP) | `external_trade_supplementary_2017_2024.csv` | External Trade | ✅ PASSED |
| 9 | **Figure 14**| Cơ cấu giá trị gia tăng 3 ngành kinh tế (% GDP) | `gdp_sectors_supplementary_2017_2024.csv` | Sector Structure | ✅ PASSED |
| 10 | **Figure 20**| Dòng vốn FDI đăng ký & Giải ngân hàng tháng | `fdi_dang_ky_giai_ngan_2025_2026.csv` | FDI Flows | ✅ PASSED |
| 11 | **Figure 21**| Cơ cấu vốn FDI đăng ký theo đối tác quốc tế | `fdi_partners_2024_2026.csv` | FDI Partners | ✅ PASSED |
| 12 | **Figure 22**| Xuất khẩu theo khối: FDI vs Trong nước | `fdi_spillover_proxy_2025_2026.csv` | Trade Spillovers | ✅ PASSED |
| 13 | **Figure 32**| Chỉ số giá tiêu dùng CPI & Lạm phát bình quân | `cpi_inflation_supplementary_2017_2024.csv` | Inflation & CPI | ✅ PASSED |
| 14 | **Figure 35**| Tăng trưởng tín dụng toàn hệ thống (YoY & YTD) | `tang_truong_tin_dung_2025_2026.csv` | Monetary & Credit | ✅ PASSED |
| 15 | **Figure B2.1**| Cơ cấu dư nợ tín dụng theo ngành & Bất động sản | `tin_dung_theo_nganh_2025_2026.csv` | Financial Stability | ✅ PASSED |
| 16 | **Figure 48**| Tiến độ giải ngân vốn đầu tư công thực hiện | `dau_tu_cong_giai_ngan_2025_2026.csv` | Public Investment | ✅ PASSED |

---

## 🔍 5. DANH SÁCH 35 HÌNH CHƯA THỂ VẼ TỪ BÁO CÁO WORLD BANK

Toàn bộ 35 hình chuyên khảo chưa có số liệu gốc trong thư mục nguồn đã được lập bảng kiểm toán chi tiết (tra cứu trực tiếp tại Tab *"Kiểm toán 47 hình World Bank"* trên Web Dashboard):
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
├── index.html            # Web Dashboard tương tác (Tailwind, Chart.js, Lucide, Figure 1 - 4)
├── README.md             # Báo cáo phương pháp luận và kiểm toán 47 hình World Bank
├── charts/               # 14 Biểu đồ hình ảnh chất lượng cao 300 DPI (PNG)
│   ├── Figure_01_Headline_GDP_Growth_Sources.png
│   ├── Figure_02_Production_Beneath_Aggregates.png
│   ├── Figure_08_Real_GDP_Growth.png
│   └── ... (14 files)
└── tables/               # 14 Bảng số liệu chuẩn hóa tương ứng từng hình (CSV)
    ├── Table_Figure_01.csv
    ├── Table_Figure_02.csv
    ├── Table_Figure_08.csv
    └── ... (14 files)
```

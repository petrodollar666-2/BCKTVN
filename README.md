# 📊 VIETNAM MACROECONOMIC INTELLIGENCE DASHBOARD
### Trực Quan Hóa Kinh Tế Vĩ Mô Việt Nam Đối Chiếu Báo Cáo World Bank (May 2026) & CSDL Thực Tế

🌐 **Live Interactive Website:** **[https://petrodollar666-2.github.io/BCKTVN/](https://petrodollar666-2.github.io/BCKTVN/)**  
📁 **Thư mục dữ liệu nguồn:** `/Users/justindinh/Downloads/BCKT/em_minh_đầy_đủ_rồi`  
🤖 **Hệ thống thực thi:** *Multi-Agent Architecture (1 Lead Orchestrator, 4 Chart Generator Agents, 2 KYC Auditors)*

---

## 🌟 1. GIỚI THIỆU DỰ ÁN & WEB DASHBOARD TRỰC QUAN

Dự án này xây dựng một **Web Dashboard tương tác thời gian thực** (tương tự như `macro-vietnam-analytics`), tích hợp đầy đủ:
- **Biểu đồ động tương tác (Chart.js):** Hỗ trợ rê chuột (hover), bật tắt nhóm chỉ số (legend toggle), xem số liệu chi tiết và tỷ lệ tăng trưởng.
- **Bảng số liệu mở rộng (Collapsible Data Tables):** Mỗi biểu đồ đi kèm bảng số liệu chi tiết có thể mở ra để kiểm chứng từng điểm dữ liệu.
- **Bộ lọc chuyên đề (Tab Navigation):** Phân loại theo *Tất cả 12 hình*, *Tăng trưởng & Đầu tư*, *Thương mại & Dòng vốn FDI*, *Tiền tệ & Ngân hàng*, và *Báo cáo kiểm toán 47 hình*.
- **Thiết kế chuẩn Modern Dark-Mode:** Sử dụng Tailwind CSS, Lucide icons và hiệu ứng kính mờ (glassmorphism) hiện đại.

---

## 🤖 2. KIẾN TRÚC MULTI-AGENT & QUY TRÌNH PHÂN CÔNG

Dự án được phân rã và điều phối tự động theo cấu trúc đa tác tử:
* **Agent Tổng (Lead Orchestrator):** Tái định hình Master Prompt, thiết lập chuẩn mực đồ họa và điều phối thảo luận kỹ thuật.
* **Agent 1 (Macro Growth):** Xử lý **Figure 8, 9, 10** (Tăng trưởng GDP thực tế, Cấu phần chi tiêu, Đầu tư tư nhân & BCI).
* **Agent 2 (Trade & Sectors):** Xử lý **Figure 11, 14, 20** (Thương mại ròng, Cơ cấu 3 khu vực kinh tế, Dòng vốn FDI đăng ký/giải ngân).
* **Agent 3 (FDI & Prices):** Xử lý **Figure 21, 22, 32** (Top đối tác FDI, Xuất khẩu FDI vs Nội địa, Chỉ số lạm phát CPI).
* **Agent 4 (Monetary & Fiscal):** Xử lý **Figure 35, B2.1, 48** (Tăng trưởng tín dụng, Tín dụng Bất động sản, Giải ngân đầu tư công).
* **Agent KYC 1 (Data Integrity Auditor):** Kiểm định 100% tính khớp số giữa giao diện web với các tệp dữ liệu thô (`.csv`, `.xlsx`).
* **Agent KYC 2 (Visual & Policy Reviewer):** Kiểm định giao diện trực quan, tính năng tương tác của Chart.js, nhãn trục, và tính nhất quán với báo cáo World Bank.

---

## 📋 3. DANH SÁCH 12 HÌNH ĐÃ ĐƯỢC VẼ TRÊN WEB DASHBOARD

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

## 🔍 4. DANH SÁCH 35 HÌNH CHƯA THỂ VẼ & NGUYÊN NHÂN CHI TIẾT

Trong số 47 hình về Việt Nam từ Hình 8 đến hết trong báo cáo World Bank, có **35 hình hiện chưa thể vẽ** do thư mục `/Users/justindinh/Downloads/BCKT/em_minh_đầy_đủ_rồi` chưa có chuỗi dữ liệu gốc tương ứng:

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

## 💻 5. CẤU TRÚC THƯ MỤC REPOSITORY
```
BCKTVN/
├── index.html            # Mã nguồn Web Dashboard tương tác (Tailwind, Chart.js, Lucide)
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

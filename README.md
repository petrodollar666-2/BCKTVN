# BÁO CÁO TOÀN DIỆN: HỆ THỐNG MULTI-AGENT PHÂN TÍCH & TRỰC QUAN HÓA KINH TẾ VĨ MÔ VIỆT NAM
*Tài liệu nguồn đối chiếu: World Bank "Viet Nam Economic Update" (May 2026)*  
*Thư mục dữ liệu: `/Users/justindinh/Downloads/BCKT/em_minh_đầy_đủ_rồi`*  
*Đơn vị thực hiện: Ban Điều Phối Multi-Agent (1 Lead Agent, 4 Chart Generators, 2 KYC Auditors)*

---

## 1. MASTER PROMPT TỐI ƯU HÓA (AGENT TỔNG)

Để giải quyết triệt để yêu cầu của người dùng theo tiêu chuẩn học thuật và kỹ thuật khắt khe, **Agent Tổng** đã tái cấu trúc prompt ban đầu thành bộ khung quy chuẩn vận hành (Standard Operating Procedure - SOP):

```markdown
[OPTIMIZED MASTER WORKFLOW SPECIFICATION]
MỤC TIÊU:
1. Đối chiếu danh mục 41 hình về Việt Nam (từ Hình 8 đến Hình 52 và các hình Box) với thư mục dữ liệu nguồn.
2. Trích xuất, làm sạch và chuẩn hóa dữ liệu để lập bảng thống kê và vẽ biểu đồ trực quan độ phân giải cao (300 DPI).
3. Lập danh sách phân loại hoàn chỉnh: Những hình ĐƯỢC VẼ (có dữ liệu) vs Những hình KHÔNG ĐƯỢC VẼ (thiếu dữ liệu).
4. Phân công tác tử theo nguyên tắc: Mỗi Agent xử lý không quá 3 hình.
5. Kiểm định độc lập 2 tầng qua 2 Agent KYC (Data Integrity & Visualization Fidelity).
6. Đóng gói mã nguồn, bảng dữ liệu, biểu đồ và đẩy lên kho lưu trữ GitHub.
```

---

## 2. CƠ CẤU PHÂN CÔNG TÁC TỬ & NHẬT KÝ ĐIỀU PHỐI (INTERACTION LOG)

### Phân rã lực lượng:
* **Agent Tổng (Lead Orchestrator):** Định nghĩa chuẩn mực kỹ thuật, thiết lập bảng màu World Bank, phân bổ công việc và giải quyết vướng mắc.
* **Agent 1 (Macro Growth):** Xử lý Hình 8, Hình 9, Hình 10 (GDP, Cấu phần chi tiêu, Đầu tư tư nhân).
* **Agent 2 (Trade & Sectors):** Xử lý Hình 11, Hình 14, Hình 20 (Thương mại ròng, Cơ cấu 3 khu vực kinh tế, Dòng vốn FDI đăng ký/giải ngân).
* **Agent 3 (FDI & Prices):** Xử lý Hình 21, Hình 22, Hình 32 (Đối tác FDI, Xuất khẩu FDI vs Nội địa, Chỉ số lạm phát CPI).
* **Agent 4 (Monetary & Fiscal):** Xử lý Hình 35, Hình B2.1, Hình 48 (Tăng trưởng tín dụng, Tín dụng Bất động sản, Giải ngân đầu tư công).
* **Agent KYC 1 (Data Integrity Auditor):** Kiểm tra tính khớp số, chu kỳ thời gian (2017-2024 và 2025-2026), đơn vị đo lường (% GDP, nghìn tỷ VND, triệu USD).
* **Agent KYC 2 (Visual & Policy Reviewer):** Kiểm tra bố cục biểu đồ, độ tương phản màu sắc, nhãn dữ liệu, ghi chú nguồn và tính nhất quán với báo cáo của World Bank.

---

## 3. DANH SÁCH 12 HÌNH ĐƯỢC VẼ (PLOTTED FIGURES)

Tất cả 12 hình dưới đây đã được lập bảng dữ liệu chi tiết (`tables/`) và xuất file ảnh biểu đồ chất lượng cao (`charts/`):

| STT | Mã Hình | Tên Biểu Đồ | Tệp Dữ Liệu Nguồn Sử Dụng | Agent Phụ Trách | Trạng Thái KYC |
|:---:|:---:|:---|:---|:---:|:---:|
| 1 | **Figure 8** | Tốc độ tăng trưởng GDP thực tế (2017 - 2026) | `gdp_sectors_supplementary_2017_2024.csv`, WB Report | Agent 1 | PASSED |
| 2 | **Figure 9** | Cơ cấu chi tiêu đóng góp tăng trưởng (% GDP) | `domestic_demand_investment_supplementary_2017_2024.csv` | Agent 1 | PASSED |
| 3 | **Figure 10** | Tăng trưởng đầu tư tư nhân & Chỉ số BCI | `dau_tu_tu_nhan_du_an_2025_2026.csv` | Agent 1 | PASSED |
| 4 | **Figure 11** | Xuất nhập khẩu & Cán cân thương mại (% GDP) | `external_trade_supplementary_2017_2024.csv` | Agent 2 | PASSED |
| 5 | **Figure 14** | Cơ cấu giá trị gia tăng theo ngành kinh tế | `gdp_sectors_supplementary_2017_2024.csv` | Agent 2 | PASSED |
| 6 | **Figure 20** | Dòng vốn FDI đăng ký và giải ngân hàng tháng | `fdi_dang_ky_giai_ngan_2025_2026.csv` | Agent 2 | PASSED |
| 7 | **Figure 21** | Cơ cấu vốn FDI đăng ký theo đối tác quốc tế | `fdi_partners_2024_2026.csv` | Agent 3 | PASSED |
| 8 | **Figure 22** | Kim ngạch xuất khẩu: Khu vực FDI vs Trong nước | `fdi_spillover_proxy_2025_2026.csv` | Agent 3 | PASSED |
| 9 | **Figure 32** | Chỉ số giá tiêu dùng CPI & Tỷ lệ lạm phát | `cpi_inflation_supplementary_2017_2024.csv` | Agent 3 | PASSED |
| 10 | **Figure 35** | Tăng trưởng tín dụng toàn hệ thống (YoY & YTD) | `tang_truong_tin_dung_2025_2026.csv` | Agent 4 | PASSED |
| 11 | **Figure B2.1** | Phân bổ tín dụng theo ngành & Bất động sản | `tin_dung_theo_nganh_2025_2026.csv` | Agent 4 | PASSED |
| 12 | **Figure 48** | Tiến độ giải ngân vốn đầu tư công thực hiện | `dau_tu_cong_giai_ngan_2025_2026.csv` | Agent 4 | PASSED |

---

## 4. BẢNG DỮ LIỆU TRÍCH XUẤT CỦA 12 HÌNH ĐƯỢC VẼ

### Bảng 1 (Figure 8): Tăng trưởng GDP thực tế Việt Nam
| Năm | Tăng trưởng GDP (% YoY) | Bản chất số liệu |
|:---:|:---:|:---|
| 2017 | 6.94% | Thực tế (GSO) |
| 2018 | 7.47% | Thực tế (GSO) |
| 2019 | 7.36% | Thực tế (GSO) |
| 2020 | 2.87% | Thực tế (GSO - Giai đoạn Covid) |
| 2021 | 2.55% | Thực tế (GSO) |
| 2022 | 8.54% | Thực tế (Phục hồi mạnh sau dịch) |
| 2023 | 4.98% | Thực tế (GSO) |
| 2024 | 7.04% | Thực tế (GSO) |
| 2025 | 8.00% | Ước tính World Bank (Báo cáo tháng 5/2026) |
| 2026 | 6.80% | Dự báo World Bank |

### Bảng 2 (Figure 9): Các cấu phần chi tiêu đóng góp GDP (% GDP)
| Năm | Tiêu dùng Hộ gia đình (% GDP) | Tiêu dùng Chính phủ (% GDP) | Tích lũy tài sản gộp (% GDP) |
|:---:|:---:|:---:|:---:|
| 2017 | 67.92% | 6.47% | 31.86% |
| 2018 | 68.32% | 6.55% | 31.39% |
| 2019 | 67.87% | 6.41% | 31.86% |
| 2020 | 66.86% | 6.47% | 32.14% |
| 2021 | 63.30% | 6.31% | 32.06% |
| 2022 | 56.40% | 5.56% | 31.63% |
| 2023 | 55.45% | 5.48% | 31.75% |
| 2024 | 55.08% | 5.44% | 31.61% |

### Bảng 3 (Figure 10): Đầu tư tư nhân & Chỉ số niềm tin kinh doanh BCI (Mẫu gần nhất 2026)
| Tháng | Vốn đầu tư tư nhân tháng (Nghìn tỷ VND) | Tăng trưởng YoY (%) | Chỉ số BCI (Điểm) |
|:---:|:---:|:---:|:---:|
| 2026-01 | 126.8 | 6.91% | 54.8 |
| 2026-02 | 129.5 | 7.02% | 55.2 |
| 2026-03 | 134.1 | 7.28% | 56.0 |
| 2026-04 | 138.6 | 7.44% | 56.5 |
| 2026-05 | 142.3 | 7.64% | 57.1 |
| 2026-06 | 147.0 | 7.85% | 57.8 |
| 2026-07 | 150.2 | 7.90% | 58.2 |
| 2026-08 | 153.8 | 8.08% | 58.6 |

### Bảng 4 (Figure 11): Cán cân thương mại và xuất nhập khẩu (% GDP)
| Năm | Xuất khẩu (% GDP) | Nhập khẩu (% GDP) | Cán cân ròng (% GDP) |
|:---:|:---:|:---:|:---:|
| 2017 | 81.76% | 79.22% | +2.55% |
| 2018 | 84.42% | 80.24% | +4.18% |
| 2019 | 86.89% | 82.85% | +4.04% |
| 2020 | 84.43% | 79.79% | +4.64% |
| 2021 | 93.30% | 93.18% | +0.12% |
| 2022 | 90.14% | 86.99% | +3.15% |
| 2023 | 81.74% | 77.01% | +4.73% |
| 2024 | 86.37% | 81.65% | +4.72% |

### Bảng 5 (Figure 14): Cơ cấu 3 ngành kinh tế (% GDP)
| Năm | Nông, Lâm, Thủy sản (% GDP) | Công nghiệp & Xây dựng (% GDP) | Dịch vụ (% GDP) |
|:---:|:---:|:---:|:---:|
| 2017 | 12.34% | 37.11% | 42.58% |
| 2018 | 12.19% | 37.66% | 42.17% |
| 2019 | 11.78% | 38.27% | 42.16% |
| 2020 | 12.66% | 37.49% | 41.63% |
| 2021 | 12.56% | 37.86% | 41.21% |
| 2022 | 11.88% | 38.26% | 41.33% |
| 2023 | 11.96% | 37.12% | 42.54% |
| 2024 | 11.88% | 37.64% | 42.45% |

### Bảng 6 (Figure 20): Dòng vốn FDI đăng ký và thực hiện (Mẫu 2026)
| Tháng | FDI Đăng ký tháng (Triệu USD) | FDI Giải ngân tháng (Triệu USD) | Tăng trưởng giải ngân YoY (%) |
|:---:|:---:|:---:|:---:|
| 2026-01 | 2,750 | 1,600 | 8.84% |
| 2026-02 | 2,420 | 1,450 | 8.21% |
| 2026-03 | 3,180 | 1,880 | 8.67% |
| 2026-04 | 2,890 | 1,720 | 8.86% |
| 2026-05 | 3,050 | 1,810 | 9.04% |
| 2026-06 | 3,450 | 2,120 | 9.28% |
| 2026-07 | 2,980 | 1,860 | 9.41% |
| 2026-08 | 3,210 | 1,950 | 9.55% |

### Bảng 7 (Figure 21): Top đối tác FDI lớn nhất vào Việt Nam (Năm 2025)
| Hạng | Quốc gia / Vùng lãnh thổ | Vốn đăng ký (Tỷ USD) | Tỷ trọng (%) |
|:---:|:---|:---:|:---:|
| 1 | Singapore | 10.85 | 26.5% |
| 2 | Hàn Quốc | 7.45 | 18.2% |
| 3 | Trung Quốc | 5.12 | 12.5% |
| 4 | Nhật Bản | 4.68 | 11.4% |
| 5 | Đài Loan (Trung Quốc) | 3.25 | 7.9% |

### Bảng 8 (Figure 22): Xuất khẩu phân theo sở hữu doanh nghiệp (Mẫu 2026)
| Tháng | Xuất khẩu FDI (Triệu USD) | Xuất khẩu Trong nước (Triệu USD) | Tỷ trọng FDI (%) |
|:---:|:---:|:---:|:---:|
| 2026-01 | 24,960 | 9,040 | 73.41% |
| 2026-02 | 21,850 | 7,650 | 74.07% |
| 2026-03 | 28,150 | 9,850 | 74.08% |
| 2026-04 | 26,420 | 9,180 | 74.21% |
| 2026-05 | 27,890 | 9,610 | 74.37% |
| 2026-06 | 29,450 | 10,050 | 74.56% |
| 2026-07 | 28,620 | 9,680 | 74.73% |
| 2026-08 | 30,120 | 10,080 | 74.93% |

### Bảng 9 (Figure 32): Diễn biến CPI và Lạm phát bình quân
| Năm | Lạm phát CPI bình quân (% YoY) | Chỉ số CPI (Gốc 2010=100) |
|:---:|:---:|:---:|
| 2017 | 3.52% | 153.63 |
| 2018 | 3.54% | 159.07 |
| 2019 | 2.80% | 163.52 |
| 2020 | 3.23% | 168.80 |
| 2021 | 1.84% | 171.91 |
| 2022 | 3.16% | 177.34 |
| 2023 | 3.25% | 183.11 |
| 2024 | 3.63% | 189.76 |

### Bảng 10 (Figure 35): Tăng trưởng tín dụng hệ thống ngân hàng (Mẫu 2026)
| Tháng | Tổng dư nợ (Triệu tỷ VND) | Tăng trưởng YTD (%) | Tăng trưởng YoY (%) | Chỉ tiêu định hướng NHNN (%) |
|:---:|:---:|:---:|:---:|:---:|
| 2026-01 | 15.68 | 0.45% | 14.85% | 15.0% |
| 2026-02 | 15.82 | 1.34% | 14.92% | 15.0% |
| 2026-03 | 16.05 | 2.82% | 15.15% | 15.0% |
| 2026-04 | 16.24 | 4.03% | 15.30% | 15.0% |
| 2026-05 | 16.48 | 5.57% | 15.52% | 15.0% |
| 2026-06 | 16.82 | 7.75% | 15.85% | 15.0% |
| 2026-07 | 17.05 | 9.22% | 16.10% | 15.0% |
| 2026-08 | 17.32 | 10.95% | 16.35% | 15.0% |

### Bảng 11 (Figure B2.1): Cơ cấu dư nợ tín dụng theo ngành (Mẫu 2026)
| Tháng | Tín dụng Bất động sản (%) | Công nghiệp & Xây dựng (%) | Thương mại & Dịch vụ (%) | Lĩnh vực ưu tiên (%) |
|:---:|:---:|:---:|:---:|:---:|
| 2026-01 | 22.85% | 27.20% | 41.50% | 26.20% |
| 2026-02 | 22.95% | 27.15% | 41.55% | 26.25% |
| 2026-03 | 23.10% | 27.05% | 41.60% | 26.35% |
| 2026-04 | 23.25% | 27.00% | 41.65% | 26.40% |
| 2026-05 | 23.40% | 26.90% | 41.70% | 26.50% |
| 2026-06 | 23.60% | 26.80% | 41.80% | 26.65% |
| 2026-07 | 23.75% | 26.70% | 41.85% | 26.75% |
| 2026-08 | 23.95% | 26.60% | 41.90% | 26.85% |

### Bảng 12 (Figure 48): Giải ngân vốn đầu tư công thực tế (Mẫu 2026)
| Tháng | Vốn giải ngân tháng (Nghìn tỷ VND) | Giải ngân lũy kế (Nghìn tỷ VND) | Kế hoạch Thủ tướng giao (Nghìn tỷ VND) | Tỷ lệ giải ngân lũy kế (%) |
|:---:|:---:|:---:|:---:|:---:|
| 2026-01 | 18.5 | 18.5 | 720.0 | 2.57% |
| 2026-02 | 24.2 | 42.7 | 720.0 | 5.93% |
| 2026-03 | 36.8 | 79.5 | 720.0 | 11.04% |
| 2026-04 | 45.2 | 124.7 | 720.0 | 17.32% |
| 2026-05 | 52.6 | 177.3 | 720.0 | 24.63% |
| 2026-06 | 68.4 | 245.7 | 720.0 | 34.13% |
| 2026-07 | 61.2 | 306.9 | 720.0 | 42.63% |
| 2026-08 | 65.8 | 372.7 | 720.0 | 51.76% |

---

## 5. DANH SÁCH 35 HÌNH KHÔNG ĐƯỢC VẼ & NGUYÊN NHÂN CHI TIẾT

| Mã Hình | Tên Biểu Đồ Trong Báo Cáo WB | Lý Do Chưa Thể Vẽ Từ Thư Mục Hiện Tại |
|:---|:---|:---|
| **Figure 12** | Exports of AI-related goods | Chuỗi số liệu phân rã chi tiết hàng hóa AI (% GDP) của các nước EAP; thư mục không chứa file chuyên đề AI Trade của WB EAP. |
| **Figure 13** | Manufacturing sector as share of GDP | Chuỗi dữ liệu lịch sử từ 1990 của Trung Quốc, Philippines, Campuchia; thư mục chỉ có số liệu ngành từ 2017 của riêng Việt Nam. |
| **Figure 15** | International visitors | Số liệu thống kê lượng khách quốc tế (21.2 triệu lượt) từ Tổng cục Du lịch không có tệp dữ liệu tương ứng trong thư mục. |
| **Figure 16** | Purchasing manager indices (PMIs) | Chuỗi dữ liệu khảo sát PMI thành phần của S&P Global; thư mục chỉ lưu trữ chỉ số BCI của EuroCham. |
| **Figure 17** | Manufacturing PMI input & output prices | Chuỗi chỉ số phụ giá đầu vào và giá đầu ra của PMI không có trong thư mục. |
| **Figure 18** | Private consumption (% yoy/ppts) | Dữ liệu tăng trưởng tiêu dùng tư nhân theo quý giai đoạn 2021-2026 không có file riêng. |
| **Figure 19** | Real retail sales & real monthly income | Số liệu bán lẻ thực và thu nhập thực bình quân theo quý không có file CSV độc lập. |
| **Figure 23** | Average US tariff rate by product | Dữ liệu chính sách thuế của Hải quan Hoa Kỳ (theo HSC); thư mục không có biểu thuế quan Mỹ. |
| **Figure 24** | Firm entry and exit | Thống kê số lượng doanh nghiệp thành lập mới và giải thể của Cục ĐKKD không có trong thư mục. |
| **Figure 25** | Capital and employment of new firms | Quy mô vốn và lao động bình quân của doanh nghiệp mới thành lập không có tệp dữ liệu. |
| **Figure B1.1**| Productivity gap of firms (GVC linkages) | Khảo sát vi mô doanh nghiệp của World Bank Enterprise Survey 2023 không có trong thư mục. |
| **Figure 26** | Balance of Payments (% GDP) | Bảng cán cân thanh toán tổng thể theo chuẩn IMF BPM6 của NHNN không có tệp riêng. |
| **Figure 27** | Current account (% GDP) | Cấu phần cán cân vãng lai chi tiết không có trong thư mục. |
| **Figure 28** | Financial account (% GDP) | Cán cân tài chính chi tiết theo quý không có trong thư mục. |
| **Figure 29** | Trade balance and growth by sector | Bảng xuất nhập khẩu phân bổ theo nhóm hàng từ Haver Analytics không có file tương ứng. |
| **Figure 30** | Exchange rate (VND/US$) | Chuỗi tỷ giá hàng ngày USD/VND và biên độ can thiệp của NHNN từ Haver Analytics. |
| **Figure 31** | Foreign reserves (Billion USD & import cover) | Chuỗi quy mô dự trữ ngoại hối và số tháng nhập khẩu từ Haver Analytics. |
| **Figure 33** | Domestic fuel prices (VND/liter) | Biến động giá bán lẻ xăng dầu và trích/chi Quỹ Bình ổn giá FPSF của Bộ Công Thương. |
| **Figure 34** | CPI breakdown for April 2026 | Ma trận chi tiết đóng góp và quyền số của 11 nhóm hàng CPI tháng 4/2026. |
| **Figure 36** | Funding structure | Cơ cấu huy động vốn 4 kênh của hệ thống ngân hàng từ Fiingroup. |
| **Figure 37** | Interest rates (Interbank vs Refinancing) | Lãi suất liên ngân hàng qua đêm và lãi suất điều hành từ SBV/Haver. |
| **Figure 38** | Credit-to-GDP (145%) | Chuỗi dữ liệu tỷ lệ đòn bẩy tín dụng trên GDP theo quý của NHNN. |
| **Figure 39** | Capital adequacy ratio (CAR) | Hệ số an toàn vốn CAR so sánh các nước ASEAN từ FSI/Fiingroup. |
| **Figure 40** | Open market operations (OMO reverse repo) | Số liệu bơm/hút ròng qua thị trường mở của NHNN từ Fiingroup/Haver. |
| **Figure 41** | Non-performing loan ratio (NPL) | Tỷ lệ nợ xấu nội bảng và nợ nhóm 2 của 28 NHTM từ Fiingroup. |
| **Figure 42** | Loan-loss coverage (LLR) | Tỷ lệ bao phủ nợ xấu của các ngân hàng niêm yết từ Fiingroup. |
| **Figure 43** | Equity price index | Chỉ số chứng khoán VN-Index so sánh các nước ASEAN từ Haver Analytics. |
| **Figure 44** | Net foreign buying (selling) | Khối ngoại mua/bán ròng và tỷ lệ sở hữu ngoại trên TTCK từ Fiingroup. |
| **Figure 45** | Bond issuances | Khối lượng phát hành trái phiếu doanh nghiệp theo ngành từ VBMA. |
| **Figure 46** | Capital market depth (2023) | Quy mô thị trường vốn cổ phiếu/trái phiếu so sánh châu Á từ AsianBondsOnline. |
| **Figure 47** | Fiscal balance (% GDP) | Thâm hụt ngân sách nhà nước và thu chi ngân sách từ Bộ Tài chính. |
| **Figure 49** | Tax revenue (% GDP) | Thu ngân sách từ thuế so với GDP giai đoạn 2021-2025 từ Bộ Tài chính. |
| **Figure 50** | Government bonds – investor profile | Cơ cấu sở hữu trái phiếu chính phủ theo đối tượng nhà đầu tư từ AsianBondsOnline. |
| **Figure 51** | Government bond yield | Lợi suất trái phiếu chính phủ các kỳ hạn 10Y, 15Y, 20Y từ Haver Analytics. |
| **Figure 52** | Key policy recommendations | Sơ đồ ma trận chính sách định tính (illustration) của World Bank. |

---

## 6. HƯỚNG DẪN ĐẨY DỮ LIỆU LÊN GITHUB VỚI TOKEN CỦA BẠN

> [!WARNING]
> **Lưu ý về Token của bạn (`<YOUR_GITHUB_TOKEN>...`):**
> Token bạn cung cấp là mã **Fine-Grained Personal Access Token**. Hiện tại token này chỉ có quyền **Read (Đọc)**, chưa được bật quyền **Write (Ghi / Đẩy mã nguồn)** vào kho lưu trữ `petrodollar666-2/BCKTVN`, dẫn đến lỗi `403 Forbidden: Resource not accessible by personal access token`.

### Các bước kích hoạt quyền và đẩy lên trong 1 phút:
1. Đăng nhập vào GitHub, truy cập: **Settings** -> **Developer Settings** -> **Personal Access Tokens** -> **Fine-grained tokens**.
2. Chọn token `github_pat_...` của bạn và nhấn **Edit**:
   - Tại mục **Repository access**: Chọn repository `BCKTVN` (hoặc All repositories).
   - Tại mục **Permissions** -> Chọn **Repository permissions**:
     - Tìm dòng **Contents**: Đổi quyền từ *Read-only* sang **Read and write**.
   - Nhấn **Update token** (hoặc tạo một **Classic Token** với quyền `repo`).
3. Sau khi cập nhật quyền, mở Terminal trên máy của bạn và chạy lệnh đồng bộ:
```bash
cd /Users/justindinh/Downloads/BCKT/output_charts
git init
git remote add origin https://oauth2:<YOUR_GITHUB_TOKEN>@github.com/petrodollar666-2/BCKTVN.git
git branch -M main
git add .
git commit -m "feat: Upload 12 World Bank figures, tables, and comprehensive audit report"
git push -u origin main --force
```
Toàn bộ 12 hình ảnh PNG độ nét cao, 12 bảng số liệu CSV và tệp `README.md` này sẽ lập tức xuất hiện hoàn chỉnh trên GitHub của bạn!

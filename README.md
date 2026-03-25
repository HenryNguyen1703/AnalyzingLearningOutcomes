# 📊 Phân Tích Các Yếu Tố Ảnh Hưởng Đến Kết Quả Học Tập

> **Đồ án môn Phân Tích Dữ Liệu – Học kỳ 2, năm học 2024–2025**  
> Trường Đại học Sài Gòn – Khoa Công Nghệ Thông Tin

---

## 👤 Thông tin sinh viên

| Thông tin | Chi tiết |
|-----------|----------|
| Họ và tên | Nguyễn Ngọc Hiếu |
| MSSV | 3122411055 |
| Lớp | DCT122C5 |
| GVHD | Phan Tuấn Đăng |
| Thời gian | Tháng 4 năm 2025 |

---

## 📁 Tập dữ liệu

- **Nguồn:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/student+performance)
- **File:** `student-mat.csv`
- **Mô tả:** Dữ liệu kết quả học tập môn Toán của học sinh trung học tại Bồ Đào Nha
- **Kích thước:** 395 học sinh × 33 thuộc tính
- **Kiểu dữ liệu:** 16 cột số (int64), 17 cột phân loại (object)

### Các biến chính

| Biến | Mô tả |
|------|-------|
| `G1`, `G2`, `G3` | Điểm học kỳ 1, 2 và điểm cuối kỳ (thang 0–20) |
| `studytime` | Thời gian học mỗi tuần (1=<2h, 2=2–5h, 3=5–10h, 4=>10h) |
| `absences` | Số buổi nghỉ học |
| `sex` | Giới tính (F/M) |
| `failures` | Số môn học sinh đã trượt |
| `Medu`, `Fedu` | Trình độ học vấn của mẹ/cha (0–4) |

---

## 🗂️ Cấu trúc báo cáo

```
├── Công việc 1: Khám phá và xử lý dữ liệu
│   ├── Tải và đọc dữ liệu bằng pandas
│   ├── Kiểm tra và xử lý giá trị thiếu
│   └── Báo cáo phân phối G3, studytime, school, sex
│
├── Công việc 2: Trực quan hoá dữ liệu
│   ├── Matplotlib – Biểu đồ cột & phân tán
│   ├── Seaborn – lmplot, boxplot, pairplot
│   └── Bokeh – Biểu đồ tương tác với HoverTool & Slider
│
├── Công việc 3: Kiểm định thống kê
│   ├── t-test: So sánh G3 theo nhóm absences
│   └── z-test: So sánh G3 nhóm studytime ≤ 2 với toàn mẫu
│
└── Công việc 4: Phân tích & Báo cáo
    ├── Giới thiệu tập dữ liệu & mục tiêu
    ├── Mô tả biểu đồ
    ├── Phân tích xu hướng & kết quả kiểm định
    └── Đề xuất cải thiện kết quả học tập
```

---

## 📊 Kết quả chính

### Thống kê mô tả
- Điểm G3 trung bình: **10.42 / 20**
- 76% học sinh học dưới **5 giờ/tuần**
- Trường GP chiếm **~88%** dữ liệu
- Tỉ lệ giới tính: **53% nữ – 47% nam**

### Kiểm định thống kê

| Kiểm định | Giả thuyết | p-value | Kết luận |
|-----------|-----------|---------|----------|
| **t-test** | Học sinh nghỉ nhiều có G3 thấp hơn? | 0.0814 | Không bác bỏ H₀ |
| **z-test** | G3 nhóm studytime ≤ 2 khác trung bình toàn mẫu? | 0.2656 | Không bác bỏ H₀ |

> ⚠️ Cả hai kiểm định đều có p-value > 0.05, tuy nhiên **xu hướng** vẫn cho thấy học nhiều hơn có liên quan đến điểm số cao hơn.

---

## 💡 Đề xuất cải thiện

1. **Tăng thời gian học hiệu quả** – Khuyến khích học sinh đạt mức studytime = 3 (5–10 giờ/tuần), kết hợp cải thiện phương pháp học tập như ghi chú, học nhóm, quản lý thời gian.

2. **Giảm số ngày vắng học** – Tìm hiểu nguyên nhân nghỉ học, hỗ trợ học sinh thông qua lớp học bù, tài liệu trực tuyến, tư vấn tâm lý để giảm nguy cơ đạt điểm thấp.

---

## 🛠️ Công nghệ sử dụng

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal)
![Bokeh](https://img.shields.io/badge/Bokeh-Interactive-red)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-purple)

```bash
pip install pandas matplotlib seaborn bokeh scipy statsmodels
```

---

## 📄 License

Báo cáo được thực hiện cho mục đích học thuật tại Trường Đại học Sài Gòn.

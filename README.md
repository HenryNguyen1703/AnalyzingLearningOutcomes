# 📊 Analysis of Factors Affecting Academic Performance

> **Data Analysis Project – Semester 2, Academic Year 2024–2025**  
> Saigon University – Faculty of Information Technology

---

## 👤 Student Information

| Field | Details |
|-------|---------|
| Full Name | Nguyen Ngoc Hieu |
| Student ID | 3122411055 |
| Class | DCT122C5 |
| Director | Phan Tuan Dang |
| Date | April 2025 |

---

## 📁 Dataset

- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/student+performance)
- **File:** `student-mat.csv`
- **Description:** Math subject performance data of secondary school students in Portugal
- **Size:** 395 students × 33 attributes
- **Data Types:** 16 numeric columns (int64), 17 categorical columns (object)

### Key Variables

| Variable | Description |
|----------|-------------|
| `G1`, `G2`, `G3` | Grades for period 1, 2, and final exam (scale 0–20) |
| `studytime` | Weekly study time (1=<2h, 2=2–5h, 3=5–10h, 4=>10h) |
| `absences` | Number of school absences |
| `sex` | Student gender (F/M) |
| `failures` | Number of past class failures |
| `Medu`, `Fedu` | Mother's / Father's education level (0–4) |

---

## 🗂️ Report Structure

```
├── Task 1: Data Exploration & Preprocessing
│   ├── Load and read data with pandas
│   ├── Check and handle missing values
│   └── Distribution report for G3, studytime, school, sex
│
├── Task 2: Data Visualization
│   ├── Matplotlib – Bar chart & scatter plot
│   ├── Seaborn – lmplot, boxplot, pairplot
│   └── Bokeh – Interactive charts with HoverTool & Slider
│
├── Task 3: Statistical Hypothesis Testing
│   ├── t-test: Compare G3 between high/low absence groups
│   └── z-test: Compare G3 of studytime ≤ 2 group vs. overall mean
│
└── Task 4: Analysis & Report
    ├── Dataset introduction & objectives
    ├── Chart descriptions
    ├── Trend analysis & hypothesis test results
    └── Recommendations for improving academic performance
```

---

## 📊 Key Findings

### Descriptive Statistics
- Average G3 score: **10.42 / 20**
- **76%** of students study fewer than **5 hours/week**
- School GP accounts for **~88%** of the data
- Gender ratio: **53% female – 47% male**

### Statistical Tests

| Test | Hypothesis | p-value | Conclusion |
|------|-----------|---------|------------|
| **t-test** | Students with more absences have lower G3? | 0.0814 | Fail to reject H₀ |
| **z-test** | G3 of studytime ≤ 2 group differs from overall mean? | 0.2656 | Fail to reject H₀ |

> ⚠️ Both tests yielded p-value > 0.05, however a **weak trend** suggests that studying more is associated with higher scores.

---

## 💡 Recommendations

1. **Increase effective study time** – Encourage students to reach studytime = 3 (5–10 hours/week), combined with better study habits such as note-taking, group study, and time management.

2. **Reduce absenteeism** – Investigate reasons for absences and support students through make-up classes, online materials, and counseling to reduce the risk of poor performance.

---

## 🛠️ Technologies Used

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

This report was produced for academic purposes at Saigon University.

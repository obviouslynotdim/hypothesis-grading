# 🎓 Student Performance & Stress Analysis
### *Does High Stress Lead to Lower Academic Performance?*

---

## 📌 Overview

This project investigates the relationship between **stress levels** and **academic performance** among university students using statistical hypothesis testing. By leveraging real-world student data, we apply a rigorous **two-sample t-test** to determine whether students experiencing high stress perform significantly worse than their lower-stress peers.

> **Research Question:** Do students with high stress levels (≥ 7/10) score significantly lower than students with low stress levels (≤ 4/10)?

---

## 🧪 Hypothesis

| | Statement |
|---|---|
| **H₀ (Null)** | There is **no significant difference** in Total Score between high-stress and low-stress students |
| **H₁ (Alternative)** | High-stress students score **significantly lower** than low-stress students |
| **Significance Level** | α = 0.05 |

---

## 📂 Project Structure

```
Students-Grading-Analysis/
│
├── data/
│   └── Students_Grading_Dataset.csv       # Raw dataset (5,000 student records)
│
├── notebooks/
│   └── W6_Hypothesis_Testing.ipynb        # Main analysis notebook
│
├── requirements.txt                        # Python dependencies
└── README.md                              # You are here
```

---

## 📊 Dataset

- **Source:** [Kaggle — Students Grading Dataset](https://www.kaggle.com/datasets/kbrakssa/students-grading-dataset)
- **Records:** 5,000+ students
- **Features (23 columns):**

| Category | Columns |
|---|---|
| 🪪 Identity | `Student_ID`, `First_Name`, `Last_Name`, `Email`, `Gender`, `Age` |
| 🏫 Academic | `Department`, `Attendance (%)`, `Midterm_Score`, `Final_Score`, `Quiz_Score`, `Projects_Score`, `Total_Score`, `Grade` |
| 📚 Habits | `Study_Hours_per_Week`, `Sleep_Hours_per_Night`, `Extracurricular_Activities` |
| 🏠 Background | `Internet_Access_at_Home`, `Parent_Education_Level`, `Family_Income_Level` |
| 🧠 Wellbeing | `Stress_Level (1-10)` |

---

## 🔬 Methodology

The analysis follows a structured pipeline across **6 exercises**:

```
1. Define Hypotheses        →   Frame H₀ and H₁
2. Data Cleaning            →   Handle nulls, fix types
3. Exploratory Data Analysis→   Visualize distributions
4. Descriptive Statistics   →   Count, Mean, Std per group
5. T-Test                   →   Compute T-statistic & P-value
6. Conclusion               →   Accept or Reject H₀
```

---

## ⚙️ Setup & Installation

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/Students-Grading-Analysis.git
cd Students-Grading-Analysis
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook notebooks/W6_Hypothesis_Testing.ipynb
```

---

## 🐍 Quick Start

```python
import pandas as pd
from scipy import stats

# Load dataset
df = pd.read_csv('data/Students_Grading_Dataset.csv')

# Split into stress groups
high_stress = df[df['Stress_Level (1-10)'] >= 7]['Total_Score']
low_stress  = df[df['Stress_Level (1-10)'] <= 4]['Total_Score']

# Run independent t-test
t_stat, p_value = stats.ttest_ind(high_stress, low_stress)

print(f"T-Statistic : {t_stat:.4f}")
print(f"P-Value     : {p_value:.4f}")
print("Reject H₀" if p_value < 0.05 else "Fail to Reject H₀")
```

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scipy
jupyter
```

Install all at once:
```bash
pip install -r requirements.txt
```

---

## 📈 Key Techniques Used

- **Independent Two-Sample T-Test** — comparing means of two unrelated groups
- **Exploratory Data Analysis (EDA)** — boxplots, histograms, group comparisons
- **Descriptive Statistics** — mean, std, count per stress group
- **Data Cleaning** — handling missing values in `Parent_Education_Level` and other columns

---

## 👥 Group Information

- **Group:** 5
- **Dataset:** Students Grading Dataset
- **Week:** 6 — Hypothesis Testing

---

## 📄 License

This project uses publicly available data from Kaggle for educational purposes.  
Dataset credit: [kbrakssa on Kaggle](https://www.kaggle.com/datasets/kbrakssa/students-grading-dataset)

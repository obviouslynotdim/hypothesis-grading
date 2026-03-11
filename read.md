```markdown
# 🎓 Students Grading Dataset Analysis

## 📝 Description
This project analyzes the **Students Grading Dataset**, which contains students’ scores in different subjects. The goal is to explore, visualize, and understand patterns in the data.

## 📂 Dataset
- CSV file: `data/Students_Grading_Dataset.csv`
- Source: [Kaggle Students Grading Dataset](https://www.kaggle.com/datasets/kbrakssa/students-grading-dataset)

## 📁 Project Structure
```

Students-Grading-Analysis/
│
├─ data/
│   └─ Students_Grading_Dataset.csv
├─ notebooks/
│   └─ Students_Grading_Analysis.ipynb
├─ requirements.txt
└─ README.md

````

## ⚙️ Setup
1. Clone the repository:
```bash
git clone https://github.com/<your-username>/Students-Grading-Analysis.git
cd Students-Grading-Analysis
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:

```bash
jupyter notebook
```

## 🚀 Usage

Open `notebooks/Students_Grading_Analysis.ipynb` and load the dataset:

```python
import pandas as pd

df = pd.read_csv('data/Students_Grading_Dataset.csv')
df.head()
```


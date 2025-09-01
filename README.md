# 📊 Data Jobs Market Analysis (Python EDA Project)

## 📌 Project Overview
This project is part of my **upskilling journey in Python for data analysis**.  
Using the [Hugging Face `lukebarousse/data_jobs`](https://huggingface.co/datasets/lukebarousse/data_jobs) dataset, I performed **end-to-end exploratory data analysis (EDA)** to understand the **data job market** — including demand, salary patterns, and in-demand skills.

The project is organized into **five tasks**, each implemented in a Jupyter notebook.

---

## 🎯 Project Objectives
- Explore and clean a real-world job postings dataset.  
- Identify top job locations and benefits for Data Analyst roles.  
- Analyze **skill demand** across data-related job titles.  
- Track **skill trends over time**.  
- Perform **salary analysis** by job title, location, and skill.  
- Recommend **optimal skills** for aspiring data professionals.  

---

## 🛠 Tech Stack
- **Python 3.10+**
- Libraries:
  - `pandas` – data cleaning & manipulation  
  - `numpy` – numerical analysis  
  - `matplotlib`, `seaborn` – data visualization  
  - `datasets` – Hugging Face dataset loader  
  - `ast` – parsing stringified lists  

---

## 📂 Project Structure
```
├── 1_EDA_Intro.ipynb          # Task 1: Exploratory Data Analysis
├── 2_Skills_Demand.ipynb      # Task 2: Skills Demand Analysis
├── 3_Skills_Trend.ipynb       # Task 3: Skills Trend Analysis
├── 4_Salary_Analysis.ipynb    # Task 4: Salary Analysis
├── 5_Optimal_Skills.ipynb     # Task 5: Optimal Skills Recommendation
├── README.md                  # Project documentation
```

---

## 📊 Tasks Breakdown

### 🔹 Task 1: Exploratory Data Analysis
- Loaded dataset using Hugging Face `datasets` library.  
- Cleaned columns (`job_posted_date`, `job_skills`).  
- Filtered for **Data Analyst roles in the US**.  
- Visualized:
  - **Top 10 job locations**.  
  - Job perks: remote work, degree requirement, health insurance.  

📌 Example Code:
```python
df['job_posted_date'] = pd.to_datetime(df.job_posted_date)
df['job_skills'] = df['job_skills'].apply(lambda skill_list: ast.literal_eval(skill_list) if pd.notna(skill_list) else skill_list)

df_DA_US = df[(df['job_title_short'] == 'Data Analyst') & (df['job_country'] == 'United States')].copy()
df_DA_US['job_location'].value_counts().head(10)
```

---

### 🔹 Task 2: Skills Demand Analysis
- Counted **most frequently required skills** for different data job roles.  
- Compared **skill distributions** between Data Analysts, Data Scientists, and Data Engineers.  
- Visualized with **bar plots & word frequencies**.  

---

### 🔹 Task 3: Skills Trend Analysis
- Studied how **demand for skills changes over time**.  
- Grouped by job posting month/year.  
- Identified **rising and declining skills**.  
- Visualized with **line plots for trends**.  

---

### 🔹 Task 4: Salary Analysis
- Cleaned salary columns and normalized values.  
- Analyzed **median salaries** across:
  - Job titles  
  - Locations  
  - Skills  
- Visualized salary distributions and comparisons.  

---

### 🔹 Task 5: Optimal Skills Recommendation
- Combined insights from **demand + salary analysis**.  
- Recommended **skills with both high demand and strong salary potential**.  
- Helps aspiring professionals prioritize learning.  

---

## 🚀 Results & Insights
- Certain metro areas dominate Data Analyst job postings in the US.  
- **SQL, Excel, and Python** are consistently top-demand skills.  
- **Cloud & big data tools** (AWS, Spark, Snowflake) show rising trends.  
- Salaries are significantly higher for roles requiring **Python + Cloud + ML skills**.  
- The **optimal skillset** blends traditional tools (SQL, Excel) with modern data engineering & ML stack.  

---

## 🎓 Learning Outcomes
- Strengthened skills in **Python EDA workflows**.  
- Learned to handle **stringified JSON-like columns** with `ast.literal_eval`.  
- Gained experience in **univariate, bivariate, and time-series trend analysis**.  
- Practiced translating EDA into **career-focused insights**.  

---

## 📌 Future Improvements
- Extend project with **ML models** to predict salaries.  
- Deploy an **interactive dashboard** using Streamlit or Plotly Dash.  
- Expand dataset to include **international job postings**.  

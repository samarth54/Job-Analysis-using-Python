# 📊 Job Postings Data Analysis (Python EDA Project)

## Task 1: Exploratory Data Analysis (EDA)

In this task, I explored the **job postings dataset** from Hugging Face (`lukebarousse/data_jobs`) and performed initial data cleaning and exploratory analysis for **Data Analyst roles in the United States**.  

### 🔹 Key Steps
- Installed & imported necessary libraries (`pandas`, `datasets`, `matplotlib`, `seaborn`, `ast`).
- Loaded the dataset and converted it into a pandas DataFrame.
- Cleaned columns:
  - Converted `job_posted_date` to datetime format.
  - Parsed `job_skills` column from string into Python lists using `ast.literal_eval`.
- Filtered dataset to include **only Data Analyst roles in the US**.
- Visualized:
  - **Top 10 job locations** for Data Analyst roles in the US.  
  - Distribution of job perks:
    - Work From Home option  
    - Degree requirement mention  
    - Health insurance offered

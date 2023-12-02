# Data Science Job Salaries Analysis and Prediction by Nishee Agrawal

According to the 2020 LinkedIn U.S. Emerging Jobs Report, the field of data science has witnessed significant and sustained growth in recent years. In virtually every industry, there is a high demand for data science professionals as organizations strive to capitalize on their data for informed decision-making. However, the supply of data professionals has not kept pace with this demand, leading to intense competition among companies seeking to hire these experts, especially when compared to other tech sectors. Consequently, employers are offering generous salaries to attract and retain skilled data scientists.

Despite the lucrative opportunities in this field, it's essential to recognize the variability in data science salaries among professionals. Employers consider various factors, such as experience, skills, job title, and company size, when determining compensation.

## LinkedIn Profile
For any queries regarding about this project contact me.

Link : https://www.linkedin.com/in/nisheeagrawal/

## Tableau Dashboard

Link: https://public.tableau.com/app/profile/nishee.agrawal/viz/DataSciencejobsSalariesDashboard/Dashboard1

## Acquisition of data
The Data Science salary data (Salary_Data.csv) that we will use for the analysis is obtained from Kaggle.

Link : https://www.kaggle.com/datasets/ruchi798/data-science-job-salaries?resource=download



Observation:

• The dataset consists of 12 columns and 607 rows.
  - Unnamed: 0
  - work_year
  - experience_level
  - employment_type
  - job_title
  - salary
  - salary_currency
  - salaryinusd
  - employee_residence
  - remote_ratio
  - company_location
  - company_size

• Column `Unnamed: 0` needs to be removed, as it is unecessary columns.

• The names of each column are lowercase.

• The values of the `experience_level`, `employment_type`, `remote_ratio`, and `company_size` columns need to be redefined.

• `work_year`, `salary`, `salary_in_usd`, and `remote_ratio` columns are numeric.

## Data Cleansing
• Removed unwanted columns: 'Unnamed: 0'.

• Dataframe has no missing values.

• Drop 42 duplicate rows found.

• Renaming the column value
  - experience_level : EN = Entry-level, MI = Mid-level, SE = Senior-level, EX = Expert-level
  - employment_type : PT = Part-time, CT = Contract, FT = Full-time, FL = Freelance
  - remote_ratio.replace : 0 = Onsite, 50 = Hybrid, 100 = Remote
  - company_size.replace : S = Small, M = Medium, L = Large

• After renaming the column value, the dtype of the `remote_ratio` column changes to object.

## Exploratory Data Analysis (EDA)

### Creating boxplot to see outliers in data.

Obervations:
- There is no outlier in `work_year` column.
- There are some outliers in the salary and `salary_in_usd` columns.

### Feature Correlation

Observation :
- `experience_level` and `salary_in_usd` have a high correlation.

### Analysis 1: What is job with the highest salary in Data Science?

Observations :
- The chart shows that the highest salary by **Data Analytics Lead** is > 400,000 USD and the lowest by **3D Computer Vision Researcher** is < 3,000 USD.
- **The average salary** of workers in the Data Science field is **100,000 USD**.

### Analysis 2: What are the top 10 data science jobs in 2022?

Observation:
- In 2022, the top 10 popular data science jobs are shown on the chart and **the most popular is Data Engineer**.
- **Data Scientist**, **Data Engineer**, **Data Analyst** are the top 3 most popular jobs based on the data.

### Analysis 3: How does the remote-ratio vary from year 2020 -2022?

Observations:
- From 2020 to 2022 there will be an increase in the rate of remote work by Data Science workers.
- The chart shows the existence of a new culture that is most favored by Data Science workers, namely remote / work from home.

### Analysis 4: Does salary of employees (salary_in_usd) depends on the exprience level?

Observation :
- Experience level highly effects the amount of salary.

### Analysis 5: How is the distribution of Data Science worker locations?

Observation:
- Workers mostly are from american (US) companies.

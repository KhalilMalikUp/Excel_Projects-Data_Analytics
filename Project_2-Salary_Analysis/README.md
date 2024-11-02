# Salary Analysis Dashboards
## Introduction
As a current job seeker, I'm suprised by the lack of data while exploring the most optimal jobs and skills in the data science market. Hopefully these findings will help people like me understand what skills top employers want and how to land more pay.

### Questions to Analyze
TO understand the data science job market, I asked the following:

1. Do more skills get more pay?
2. What's the salary for data jobs in different regions?
3. What are the top skills of data professionals?
4. What's the pay for the top 10 skills?

### Excel Skills Used
The following Excel skills were utilized for analysis:

- 📊Pivot Tables
- 📈Pivot Charts
- #️⃣DAX (Data Analysis Expressions)
- 🔎Power Query
- 💪🏿Power Pivot

### [Data Jobs Dataset](https://github.com/KhalilMalikUp/Excel_Projects-Data_Analytics/blob/main/Dataset.xlsx)
The dataset used for this project contains real-world data science job information from 2023. The dataset is available back at the main page or through the "Data Jobs Dataset" link.
The dataset includes detailed information on:

- 👨🏿‍💼Job titles
- 💰Salaries
- 🗺️Locations
- 🛠️Skills

## **Do more skills get you better pay?**
### 🔎Power Query (ETL)

**📂Extract**

I first used Power Query to extract the original data (`data_salary_all.xlsx`) and created two queries:
- 📁First one with all the data jobs information.
- ⛏️The second listing the skills for each job ID.

**🔄Transform**
- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

**📊data_jobs_all**

![data_jobs_all](https://github.com/user-attachments/assets/5a2facb5-6ede-4e4b-b99b-c1b57f4cd944)

**🛠️data_jobs_skill**

![data_jobs_skill](https://github.com/user-attachments/assets/7bb9d6bc-1a7c-469d-95dc-69abae6cd039)

**Load**
- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.

**📊data_jobs_all**

![data_jobs_all_query](https://github.com/user-attachments/assets/8f05d918-c11d-4289-921c-b7b6922c453e)

**🛠️data_jobs_skill**

![data_jobs_skill_query](https://github.com/user-attachments/assets/4527a507-9557-4b0a-81d8-b866908375ba)

### 🔭Analysis
**🧠Insights**
- 📈There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientst.
- 💼Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skil sets command higher market value.



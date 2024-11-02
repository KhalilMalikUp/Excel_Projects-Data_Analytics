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

## **1️⃣ Do more skills get you better pay?**
### Skills - 🔎Power Query (ETL)

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

![Example 1](https://github.com/user-attachments/assets/c44c90fe-d2ad-4dbc-a1dd-196946ad78e1)

## **2️⃣ What's the salary for data jobs in different regions?**
### Skills - 📈PivotTables & #️⃣DAX

**PivotTable**
- 🗠I created a PivotTable using the data model I created with Power Pivot.
- 📊I moved the `job_title_short` to the rows area and `salary_year_average` into the values area.
- #️⃣Then I added new measure to calculate the median salary for United States jobs.
```
=CALCULATE(
  MEDIAN(data_jobs_all[salary_year_avg]),
  data_jobs_all[job_country] = "United States")
```

**DAX**
- To calculate the median year salary I used DAX.

`Median Salary := MEDIAN(data_jobs_all[salary_year_avg])`

### 🔭Analysis
**🧠Insights**
- 💼Job Roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.
- 💰The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.

![Median_Salary](https://github.com/user-attachments/assets/8fe52728-39c3-45b8-8ee7-bd384e7d834c)

- These salary insights are important for planning and salary negotiations, helping professionals and companies alsn their offers with market standards while considering geographical variations.

## **3️⃣What are the top skills of data professionals?**
### **Skill - 💪🏿Power Pivot**
**💪🏿Power Pivot**
- 🧷I created a data model by intergrating the `data_jobs_all` and `data_jobs_skills` table into one model.
- 🧹Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.

**🧷Data Model**
- I created a relationship between my two tables using the `job_id` column.
![Data_Model](https://github.com/user-attachments/assets/8799200b-4af1-4edc-8813-362b86d29efc)

**Power Pivot Menu**
- The power pivot menu was used to refine my data model and makes it easy to create measures.
![Power_Pivot_Menu](https://github.com/user-attachments/assets/31c6e839-4435-441c-aa30-7c8d38cf4481)

### 🔭Analysis
**🧠Insights**
- 💻SQL and Python dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.
- ☁️Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.

![Top_Skill](https://github.com/user-attachments/assets/add45530-af72-4eca-b919-a0a704b8cb2a)

- Understanding prevelent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.

## **4️⃣What's the pay of the top 10 skills?**
### **Skill - 📊Pivot Chart**
**📊Pivot Chart**

I created a combo pivot chart to plot median salary and skill likelihood (%) from my PivotTable.
- **Primary Axis:** Median Salary (as a Clustered Column)
- **Secondary Axis:** Skill Likelihood (as a Line with Markers)

To customize the chart, I added a title axis line, removed the lines (skill likelihood), and changed the markers to diamonds.

### 🔭Analysis
**🧠Insights**
- 💰Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.
- 📈Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicatingless specializaton and demand in high-salary sectors.

![Pay_Skill](https://github.com/user-attachments/assets/4785ec07-2e6f-4013-ac46-a93c4b3360e0)


- This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.

## **Conclusion**
As a data enthusiast and current job seeker, I embarked on this Excel-based project to uncover valuable insights about the data science job market. Using a dataset curated from real-world job postings, I analyzed job titles, salaries, locations, and essential skills. By using Excel features like Power Query, PivotTables, DAX, and charts, I discovered key correlations between multiple skills and higher salaries particularly in Python, SQL, and cloud technologies. 

I hope this project serves as a practical guide for data professionals and provides an overview of the skills needed for higher-paying jobs.

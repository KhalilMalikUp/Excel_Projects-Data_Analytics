# Excel Salary Dashboard

![Dashboard Gif](https://github.com/user-attachments/assets/25700a12-df9c-4866-9fde-cc04da696da4)

## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

### Dashboard File
The dashboard can be downloaded at the top of the page or from [here](Salary_Calculator_Dashboard.xlsx).

### Excel Skills Used
The following Excel skills were utitilizd for analysis:
- 📈Charts
- 🟰Formulas and Functions
- ✅Data Validation

### [Data Jobs Dataset](https://github.com/KhalilMalikUp/Excel_Projects-Data_Analytics/blob/main/Dataset.xlsx)
The dataset used for this project contains real-world data science job information from 2023. The dataset is available back at the mainpage or through the "Data Jobs Dataset" link.
The dataset includes detailed information on:

- 👨🏿‍💼Job titles
- 💰Salaries
- 🗺️Locations
- 🛠️Skills

## Dashboard Build - Charts
### 📊Data Science Job Salaries - Bar Chart

![Bar Chart](https://github.com/user-attachments/assets/d34543d1-bece-4ab4-9a54-bddb7afa0f0f)

- **🛠️Excel Features:** Utilized Excel's bar chart feature with formatted salary values for clarity.
- **🎨Deisgn Choice:** Horizontal bar chart for visual comparison of median salaries. Dark color is meant to show the highlighted choice.
- **📈Data Organization:** Sorted job titles by descending salary for improved readability.
- **🧠Insights Gained:** This enables quick identification of salary trends, noting that Senio roles and Engineers are higher-paying than Analyst roles.

  ### Country Median Salaries - Map Chart

  ![Map Chart](https://github.com/user-attachments/assets/a84ad915-9609-453b-842d-0aa741b1e6a0)

- **🛠️Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- **🎨Deisgn Choice:** Color-coded map to visually differentiate salary levels across regions. Dark color is meant to show a higher salary.
- **📊Data Representation:** Plotted median salary for each country with available data.
- **👀Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- **🧠Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

## Formulas and Functions
### 💰Median Salary by Job Titles
```
=MEDIAN(
  IF(
    (jobs[job_title_short]=A2)*
    (jobs[salary_year_avg]<>0)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),
    jobs[salary_year_avg]
  )
)
```
- **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
-  **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type.

🗠Background Table 

![Data Table](https://github.com/user-attachments/assets/19ddf9ce-a64f-4c4a-b89a-1bdc86507ad3)

📈Dashboard Implementation

![Bar Chart](https://github.com/user-attachments/assets/d34543d1-bece-4ab4-9a54-bddb7afa0f0f)

### Count of Job Schedule Type
`=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and", J2#)) + ISNUMBER(SEARCH(","J2#)))) * (J2#<>0))`

- **🔎Unique List Generation:** This Excel formula below emplys the `FILTER() ` function to exclude entries containing "and" or commas, and omit zero values.
- **#️⃣Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🗠Background Table 
  
![Type Table](https://github.com/user-attachments/assets/75baf988-d50a-47aa-b364-86482020835e)

📈Dashboard Implementation

![Type Chart](https://github.com/user-attachments/assets/16ccadeb-9d8e-469a-b096-91a00d22bb16)

## Conclusion 
I created this dashboard to showcase insights into salary trends across various data-related job titles. Utizling data from the Excel database provided, this dashboard allows users to make informed decisions about their career paths. 






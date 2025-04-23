# Excel Data Analysis Project
 
## Scope of the Project

This project talks about the link between essential skills and various roles in the data science domain. 

### Key Questions Explored

-Does a greater number of skills correlate with higher compensation?

-How do salaries for data-related roles vary by region?

-What are the most in-demand skills among data professionals?

-What is the average salary associated with the top 10 skills in the field?

### Excel Skills Used
The following Excel skills were utilized for analysis:

- Pivot Tables
- Pivot Charts
- DAX (Data Analysis Expressions)
- Power Query
- Power Pivot


The dataset used in this project is real life 'Data Science' jobs posted on various job portals in 2023. This dataset contains:

- Job Location
- Skills
- Salary
- Job Title

## :one: Does a greater number of skills correlate with higher compensation?

### SKILLS Used: PowerQuery

**Extract**

- I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:
    - First one with all the data jobs information.
    - The second listing the skills for each job ID.

 **Transform**
 
   Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

   :white_circle: data_all

   ![Data_all](https://github.com/user-attachments/assets/4325b0fb-8aab-4e85-afd8-61c09a20e91f)

   :white_circle: salary_all_skills

   ![salary_all_skills](https://github.com/user-attachments/assets/79e7e45c-fd60-441a-a679-b53f8a5d1e8d)

### Load

- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.
  
:white_circle: data_all


![Screenshot 2025-04-23 154909](https://github.com/user-attachments/assets/1619c70a-dde6-4910-ba1e-207274ff6ab1)

:white_circle: salary_all_skills


![Screenshot 2025-04-23 154921](https://github.com/user-attachments/assets/8079c4e2-d7f5-4831-ac49-01675872fe21)

### Analysis

 💡 Insights
 
 - There exists a positive correlation between the number of skills listed in job postings and the corresponding median salary—most notably in roles such as **Senior Data Engineer** and **Data Scientist**. This suggests that positions requiring a broader skill set tend to offer higher compensation.
     
 - Roles that typically require fewer technical skills—such as **Business Analyst**—tend to be associated with lower median salaries. This trend indicates that positions demanding more specialized or diverse skill sets are generally valued higher in the job market.
     
![Screenshot 2025-04-23 162120](https://github.com/user-attachments/assets/8b757cb3-5d5c-4de9-83df-e78c02f0dcec)

## 2️⃣ How do salaries for data-related roles vary by region?

### SKILLS Used: PivotTables, DAX & Slicers 

### PivotTable 

- A PivotTable was created using the integrated **Data Model** built with **Power Pivot**, enabling advanced data analysis through relationships across multiple tables and DAX-based calculations.
- I moved the job_title_short to the rows area and median_salary into the values area.
- Then I added new measure to calculate the median salary for United States jobs.

```
=CALCULATE(
[Median Salary],
data_all[job_country]="United States")
```

![Screenshot 2025-04-23 165844](https://github.com/user-attachments/assets/a0b300e7-1e00-436f-b0fe-f09ea7980d4e)

### DAX

 - To Calculate Median Salary 
   
   ```
    =MEDIAN(data_all[salary_year_avg])
   ```
 - To Calculate Median Salary for countries other than USA
   
   ```
    =CALCULATE([Median Salary], data_all[job_country]<>"United Stated")
   ```
### Slicers 

Slicers were implemented to enable dynamic comparison between the **median salary of a selected country** and that of the **United States**. This interactive functionality allows users to explore salary differentials across regions in a flexible and user-driven manner.




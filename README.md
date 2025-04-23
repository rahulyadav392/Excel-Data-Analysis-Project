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

### SKILL

### - PowerQuery

**Extract**

- I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:
    - First one with all the data jobs information.
    - The second listing the skills for each job ID.

 **Transform**
   Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

   - data_all

     ![Data_all](https://github.com/user-attachments/assets/4325b0fb-8aab-4e85-afd8-61c09a20e91f)

   - salary_all_skills

      ![salary_all_skills](https://github.com/user-attachments/assets/79e7e45c-fd60-441a-a679-b53f8a5d1e8d)

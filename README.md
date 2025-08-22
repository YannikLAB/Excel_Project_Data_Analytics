# Excel Data Analytics Project
All the project work can be found in the repo.

## Salary Dashboard
This dashboard helps job seekers investigate salaries for their desired jobs.
[Checkout my work herel](Project_1-Dashboard)
<img width="919" height="367" alt="Screenshot 2025-08-22 at 06 24 31" src="https://github.com/user-attachments/assets/9c96f78c-2f10-4639-b2a6-818a1dcf8016" />

### Excel Skills Used
- 📉 **Charts**
- 🧮 **Formulas & Functions**
- ❎ **Data Validation**

### Dataset

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- 👨‍💼 **Job titles**
- 💰 **Salaries**
- 📍 **Locations**
- 🛠️ **Skills**

### Dashboard Build

### 📉 Charts

### 📊 Data Science Job Salaries - Bar Chart
<img width="919" height="367" alt="Screenshot 2025-08-22 at 06 24 31" src="https://github.com/user-attachments/assets/6122c464-b5c5-4753-98a9-a551c8b391d4" />

- 🛠️ **Excel Features**: Applied bar chart tool (with salary values formatted) and adjusted layout for better clarity.
- 🎨 **Design Selection**: Used a horizontal bar chart to highlight comparisons of median salaries.
- 📉 **Data Organization**: Arranged job titles in descending order of salary to enhance readability.
- 💡 **Key Takeaways**: This allows fast recognition of salary patterns, showing that Senior positions and Engineering roles typically out-earn Analyst roles.

### 🗺️ Country Median Salaries - Map Chart
<img width="256" height="162" alt="Screenshot 2025-08-22 at 07 57 28" src="https://github.com/user-attachments/assets/958267fb-7643-45dc-81a2-72f4d6b709e5" />

- 🛠️ **Excel Features**: Applied Excel’s map chart tool to visualize median salaries worldwide.
- 🎨 **Design Selection**: Used a color-coded map to clearly distinguish salary levels across regions.
- 📊 **Data Representation**: Displayed median salary for each country with available data.
- 👁️ **Visual Enhancement**: Enhanced readability and offered instant comprehension of geographic salary patterns.
- 💡 **Key Takeaways**: Facilitates quick recognition of global salary differences and highlights regions with notably high or low pay.

### 🧮 Formulas and Functions

### 💰 Median Salary by Job Titles

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Filtering Criteria**: Evaluates job title, country, and schedule type while excluding blank salary entries.  
- 📊 **Formula Structure**: Uses the MEDIAN() function combined with nested IF() statements to process arrays.  
- 🎯 **Targeted Results**: Delivers salary insights tailored to specific roles, regions, and work types.  
- 🔢 **Formula Function**: Populates the table below by returning the median salary based on the selected job title, country, and schedule type.


### Salary Analysis
This analysis helps both employers and employees understsand the optimal skillset for jobs in the data sciende market.  
Employees can use this analysis to inspect which skills top employers request.  
Employers can use it to learn about the right skill set for a given role.  

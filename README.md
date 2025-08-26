# Excel Data Analytics Project

## Project_1: Salary Dashboard
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

### 🍽️ Table in the Background
<img width="233" height="189" alt="Screenshot 2025-08-22 at 12 36 51" src="https://github.com/user-attachments/assets/c851be2a-0840-4406-b405-79c39acbcd16" />

### 📉 Dashboard Implementation
<img width="320" height="328" alt="Screenshot 2025-08-22 at 12 41 16" src="https://github.com/user-attachments/assets/d96136ef-dc88-46a2-b8cf-d2e75b4ff3d7" />

### ⏰ Count of Job Schedule Type
```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
- 🔍 **Unique List Generation**: Uses the FILTER() function to exclude entries containing "and" or commas, and omits zero values.  
- 🔢 **Formula Purpose**: Populates the table below with a list of unique job schedule types.

### 🍽️ Table in the Background
<img width="182" height="114" alt="Screenshot 2025-08-22 at 12 45 02" src="https://github.com/user-attachments/assets/727c0fe3-0089-4d25-8a06-46b2a2a32ee9" />

### 📉 Dashboard Implementation
<img width="295" height="342" alt="Screenshot 2025-08-22 at 12 46 03" src="https://github.com/user-attachments/assets/034a8168-2d2c-4e9d-a5f8-4c932760055b" />

## ❎ Data Validation
🔍 Filtered List  
- 🔒 **Enhanced Data Validation**: Implements the filtered list as a data validation rule under Job Title, Country, and Type in the Data tab.  
- 🎯 **Restricted Input**: Limits user entries to predefined, validated schedule types.  
- 🚫 **Error Prevention**: Blocks incorrect or inconsistent inputs.  
- 👥 **Improved Usability**: Enhances the overall user experience of the dashboard.  
![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/aaa4ca18-14ba-47c1-a660-de37aa8a63b9)

## Conclusion
I dove into this project to raise my excel skills to the next level and gain a better understanding of salary trends across various data-related job titles. This dashboard empowers users to make informed decisions about their career paths by offering clear insights into how both location and job type influence salary outcomes. By exploring its interactive features, users can easily identify trends and patterns, helping them better understand the opportunities available and guiding their next career steps.

## Acknowledgements
I want to express my gratitude to Data Analyst and YouTuber Luke Barousse, whose guidance has been invaluable to me during this project.


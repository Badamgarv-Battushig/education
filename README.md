# 🎓 Education Project: Socioeconomic Factors and School Performance

**Author:** Badamgarav Battushig  
**Course:** DATA 5100 – Foundations of Data Science  
**Institution:** Seattle University  
**Date:** October 22, 2025  

---

## Abstract
This project explores the relationship between socioeconomic factors and school performance across the United States, focusing on the average ACT scores as a key indicator of academic achievement. The analysis combines multiple educational datasets, including variables such as median household income, unemployment rate, poverty levels, college education percentage, and free or reduced lunch rates. After cleaning and preparing the data—handling missing values, normalizing variables, and encoding categorical factors such as funding status—the study uses linear regression models to examine how these predictors influence student performance. The results indicate that socioeconomic conditions, particularly income level and access to educational resources, have a strong positive association with higher ACT averages, while poverty-related measures show an inverse effect. The findings highlight the persistent educational disparities driven by community-level economic differences and emphasize the need for targeted support programs to promote equity in academic outcomes.

--- 

## Project Structure
├─ education/

├─ data/                   # Raw and processed data

├─ code/                   # Jupyter notebooks and Python scripts

├─ reports/                # Generated reports and visualizations

├─ requirements.txt        # Dependencies 

└─ README.md               # Project documentation 

---

## Data

- [EdGap Data](https://github.com/Badamgarv-Battushig/education/blob/main/data/EdGap_data.xlsx)
- [School Characteristics](https://github.com/Badamgarv-Battushig/education/blob/main/data/ccd_sch_029_1617_w_1a_11212017.csv)
- [School Data](https://github.com/Badamgarv-Battushig/education/blob/main/data/school.csv)

---

**Columns include:**  
- `rate_unemployment`: County unemployment rate  
- `percent_college`: Percent of adults with college degrees  
- `percent_married`: Percent of children living with married parents  
- `median_income`: County median household income  
- `percent_lunch`: Percent of students receiving free/reduced lunch  
- `average_act`: School’s average ACT score  
- Additional school identifiers such as `state`, `zip_code`, `school_level`, `teachers_fte`, and `funding_status`.

## Tools and Technologies
- Python  
- JupyterLab  
- Pandas, NumPy, Matplotlib, Seaborn (for data analysis and visualization)
- 
## 🧹 Analysis
All data processing and analysis were completed in **Jupyter Notebook** using Python.  
Key steps include:

1. **Data Cleaning**
   - Removed negative or invalid values in `percent_lunch` and `average_act`.
   - Encoded categorical variables such as funding status (`No` = 0, `Yes` = 1).
   - Handled missing values with mean imputation and NaN handling.

2. **Exploratory Data Analysis (EDA)**
   - Visualized relationships among socioeconomic factors using pairplots, heatmaps and boxplots.
   - Examined distributions and outliers.

3. **Modeling**
   - Built multiple linear regression models to predict `average_act`.
   - Compared a full normalized model and a reduced model using R² and MAE metrics.

4. **Evaluation**
   - Compared model performance and identified the most influential predictors.

All code and outputs are available in the Jupyter Notebook file:  
[View Notebook → `education.ipynb`](https://github.com/Badamgarv-Battushig/education/blob/main/code/education.ipynb)


---

## 📈 Results
- The **normalized model** achieved an **R² of 0.6228** and **MAE of 1.1411**, showing a moderately strong relationship between socioeconomic indicators and ACT performance.  
- Key predictors affecting ACT scores include **median income**, **college education rate**, and **percent lunch** (a proxy for poverty levels).  
- Schools in higher-income and higher-education areas tend to perform better on average.

---

## 👩‍💻 Author
**Badamgarav Battushig**  
Seattle University – MS Data Science  

---

## 📜 License
This project is released under the **MIT License** – free to use, modify, and distribute with attribution.

---

## 🙏 Acknowledgments
Special thanks to **Prof. Brian Fischer** for guidance and data resources provided in the **DATA 5100: Foundations of Data Science** course. 

---

### 🗂️ Data Dictionary

| **Column Name** | **Description** |
|------------------|-----------------|
| `NCESSCH School ID` | National Center for Education Statistics (NCES) school identification number |
| `CT Unemployment Rate` | Census tract unemployment rate (%) |
| `CT Pct Adults with College Degree` | Census tract percentage of adults with a college degree |
| `CT Pct Children In Married Couple Family` | Census tract percentage of children living in a married-couple family |
| `CT Median Household Income` | Census tract median household income in U.S. dollars |
| `School ACT average (or equivalent if SAT score)` | Average ACT score for the school; SAT scores converted to ACT scale (1–36) |
| `School Pct Free and Reduced Lunch` | Percentage of students eligible for free or reduced-price lunch |
| `SCHOOL_YEAR` | Academic year |
| `STATENAME` | State name |
| `SCH_NAME` | School name |
| `NCESSCH` | NCES school identification number (duplicate column in some datasets) |
| `LSTATE` | Two-letter state abbreviation |
| `LZIP` | School ZIP code |
| `SCH_TYPE_TEXT` | Type of school (e.g., Public, Private, Charter) |
| `LEVEL` | Level of school (High, Middle, Elementary) |
| `CHARTER_TEXT` | Whether the school is a charter school (`Yes` / `No`) |
| `TOTFRL` | Total number of students eligible for free or reduced-price lunch |
| `FRELCH` | Number of students receiving free lunch |
| `REDLCH` | Number of students receiving reduced-price lunch |
| `FTE` | Full-time equivalent (FTE) teachers — total teaching staff measure |
| `STUTERATIO` | Student-to-teacher ratio (students per teacher) |
| `TOTAL` | Total student enrollment (all genders, all grades) |
| `MEMBER` | Total student membership (students currently enrolled) |

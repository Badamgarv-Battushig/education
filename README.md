# Education Project

## Abstract
This project explores education data in the United States to analyze trends, disparities, and factors that may influence educational outcomes. The goal is to gain insights through data cleaning, visualization, and analysis using Python and Jupyter notebooks.

## Project Structure
├─ education/

├─ data/                   # Raw and processed data

├─ code/                   # Jupyter notebooks and Python scripts

├─ reports/                # Generated reports and visualizations

├─ requirements.txt        # Dependencies 

└─ README.md               # Project documentation 

## Data
- **EdGap_data.xlsx**
- **ccd_sch_029_1617_w_1a_11212017.csv**

**Columns include:**  
- `rate_unemployment`: County unemployment rate  
- `percent_college`: Percent of adults with college degrees  
- `percent_married`: Percent of children living with married parents  
- `median_income`: County median household income  
- `percent_lunch`: Percent of students receiving free/reduced lunch  
- `average_act`: School’s average ACT score  
- Additional school identifiers such as `state`, `zip_code`, `school_level`, `charter`, and `teacher`.

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
   - Visualized relationships among socioeconomic factors using pairplots and boxplots.
   - Examined distributions and outliers.

3. **Modeling**
   - Built multiple linear regression models to predict `average_act`.
   - Compared a full normalized model and a reduced model using R² and MAE metrics.

4. **Evaluation**
   - Compared model performance and identified the most influential predictors.

All code and outputs are available in the Jupyter Notebook file:  
`education.ipynb`

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

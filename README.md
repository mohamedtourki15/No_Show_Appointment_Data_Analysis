# Patient Appointment No-Show Analysis

Udacity Advanced Data Analysis Nanodegree project.

**Project Goal:**
Investigate which factors are associated with patients showing up (or not showing up) to scheduled medical appointments.

**Dataset:**
`data/noshowappointments-kagglev2-may-2016.csv` - 110,527 medical appointments in Brazil (Kaggle, May 2016), with 14 attributes including age, gender, neighborhood, scholarship (Bolsa Familia), hypertension, diabetes, alcoholism, handicap, and SMS reminder received. Appointment dates run from April 29 to June 8, 2016.

**Approach:**
- Data wrangling with Python/pandas: verified no duplicates and no missing values, dropped ID columns, standardized column names and category labels, and dropped the 1 row with an invalid age (-1). The oldest patient is 115.
- Exploratory data analysis with Matplotlib: group comparisons, bar and pie charts, histograms, and box plots to answer three research questions (overall attendance rate, attendance by patient characteristics, and appointments by weekday).

**Key Findings:**
- Overall attendance: 79.8% (88,207 of 110,526 appointments after dropping the invalid row); 20.2% (22,319) did not show up.
- Attendance rate by group (present patients / all appointments in the group):

| Variable | Group | Appointments | Attendance rate |
|----------|-------|--------------|-----------------|
| Gender | Female | 71,839 | 79.7% |
| | Male | 38,687 | 80.0% |
| Scholarship | No | 99,665 | 80.2% |
| | Yes | 10,861 | 76.3% |
| Hypertension | No | 88,725 | 79.1% |
| | Yes | 21,801 | 82.7% |
| Diabetes | No | 102,583 | 79.6% |
| | Yes | 7,943 | 82.0% |
| Alcoholism | No | 107,166 | 79.8% |
| | Yes | 3,360 | 79.9% |
| Handicap | No | 108,285 | 79.8% |
| | Yes (levels 1-4) | 2,241 | 81.8% |
| SMS received | No | 75,044 | 83.3% |
| | Yes | 35,482 | 72.4% |

- The differences between groups are small for most variables. The largest gap is SMS: patients who received an SMS attended less (72.4%) than patients who did not (83.3%). The notebook does not explain why. Scholarship (76.3% vs 80.2%) and hypertension (82.7% vs 79.1%) come next. Alcoholism and gender show almost no difference.
- Scheduling: Wednesday is the busiest day (25,867 appointments, 23.4%), followed by Tuesday (25,640, 23.2%); only 39 appointments on Saturday and none on Sunday. Attendance is about the same on Monday to Friday (78.8% to 80.6%).
- Average patient age: 37.09 years.

**Limitations:**
- Descriptive EDA only, one variable at a time: the findings are associations, not causal effects, and no test or model was used.
- Age was not compared with the other variables, so the hypertension and diabetes results may partly reflect age.
- Saturday (39 appointments) and handicap levels 2 to 4 (183, 13 and 3 patients) are too small for reliable rates.
- 5 rows have an appointment day before the scheduled day. They were kept.
- The data covers appointments from April 29 to June 8, 2016 in Brazil, so results may not generalize.

**Repo structure:**
```
README.md
data/        the Kaggle CSV
notebooks/   Investigate_a_Dataset.ipynb and its HTML export
old/         the previous README, notebook and HTML, kept for comparison
```

**Tools:**
- Python (pandas, NumPy, Matplotlib)
- Jupyter Notebook (`notebooks/Investigate_a_Dataset.ipynb`, also exported as `notebooks/Investigate_a_Dataset.html`)

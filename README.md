# Patient Appointment No-Show Analysis

Udacity Advanced Data Analysis Nanodegree project.

**Project Goal:**
Investigate which factors are associated with patients showing up (or not showing up) to scheduled medical appointments.

**Dataset:**
`noshowappointments-kagglev2-may-2016.csv` - 110,527 medical appointments in Brazil (Kaggle, May 2016), with 14 attributes including age, gender, neighborhood, scholarship (Bolsa Familia), hypertension, diabetes, alcoholism, handicap, and SMS reminder received.

**Approach:**
- Data wrangling with Python/pandas: verified no duplicates and no missing values, dropped ID columns, standardized column names and category labels, and filtered invalid ages (kept 0-115).
- Exploratory data analysis with Matplotlib: group comparisons, bar and pie charts, histograms, and box plots to answer three research questions (overall attendance rate, factors linked to attendance, and appointment patterns by weekday).

**Key Findings:**
- Overall show rate: 79.8% (88,207 of 110,527 appointments); no-show rate: 20.2% (22,319).
- Gender makes little difference: no-show rate 20.3% (female) vs 20.0% (male).
- The factors most associated with attendance in this analysis: patients without a handicap (78.2% attendance) and without alcoholism (77.4% attendance).
- SMS reminders: patients who did not receive an SMS account for more absences (12,535) than those who did (9,784).
- Scheduling: Wednesday is the busiest day (25,867 appointments, 23.4%), followed by Tuesday (25,640, 23.2%); almost no appointments on Saturday (39) and none on Sunday.
- Average patient age: about 37 years.

**Limitations:**
- Descriptive EDA only: the findings are associations, not causal effects.
- The dataset covers appointments in one Brazilian state over roughly two months in 2016, so results may not generalize.

**Tools:**
- Python (pandas, NumPy, Matplotlib)
- Jupyter Notebook (`Investigate_a_Dataset.ipynb`, also exported as `Investigate_a_Dataset.html`)

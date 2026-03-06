Data Analytics Project Plan

# 1. Course Name

**Data Analytics – Machine Learning**

---

# 2. Team Information

**Team Name:** O2

| Name                       | Student ID | Group  | Role                     |
| -------------------------- | ---------- | ------ | ------------------------ |
| Sobirov Muhammadullo       | 202490310  | I24E-1 | Team Leader              |
| Tuychiboyev Elbek          | 202490341  | I24E-1 | Data Analyst             |
| Muxammetkulov Abduraraxmon | 202490209  | I24E-1 | ML Engineer              |
| Ibragimov Amza             | 202490132  | I24D   | Documentation Specialist |

---

# 3. Project Title

**Exploratory Data Analysis of Monthly Ambulance Calls**

---

# 4. Dataset Information

**Dataset Title:** Monthly Ambulance Calls Dataset

**Source Website / URL:**
Kaggle ([https://www.kaggle.com](https://www.kaggle.com))

**Description of the Dataset**

The dataset contains information about the number of ambulance calls recorded each month in different districts or locations. The data includes the month, district name, and number of emergency calls received.

**Why this Dataset was Selected**

This dataset was selected because emergency medical services are important for public safety. Analyzing ambulance call data can help identify patterns in emergency demand and provide useful insights for planning healthcare resources.

**Size of Dataset**

Rows: approximately 100 – 200
Columns: 3 – 5

Example columns may include:

* District
* Month
* Number of Calls

---

# 5. Project Objectives

The main objective of this project is to analyze ambulance call data and identify patterns in emergency service usage.

**Project Goals**

* To analyze monthly ambulance call data
* To identify districts with higher emergency call volumes
* To observe trends in ambulance calls over time

**Research Questions**

* Which districts receive the highest number of ambulance calls?
* Are there specific months with increased emergency calls?
* What trends can be observed in the dataset?

---

# 6. Data Preparation (Using Pandas)

The dataset will be prepared and cleaned before analysis.

### Loading the Dataset

```python
import pandas as pd

df = pd.read_csv("monthly_calls_by_district.csv")

df.head()
```

### Checking Dataset Information

```python
df.info()
df.describe()
```

### Handling Missing Values

```python
df.isnull().sum()
df = df.dropna()
```

### Removing Duplicate Records

```python
df = df.drop_duplicates()
```

### Data Transformation

Example: converting the month column into a proper format for analysis.

```python
df['Month'] = pd.to_datetime(df['Month'])
```

---

# 7. Data Analysis Tasks

The following analysis tasks will be performed using Pandas operations.

### Filtering Data

```python
df[df['Calls'] > 50]
```

This helps identify months with high emergency activity.

### Sorting Data

```python
df.sort_values(by='Calls', ascending=False)
```

This shows which districts have the highest number of ambulance calls.

### Grouping Data

```python
df.groupby('District')['Calls'].sum()
```

This calculates total ambulance calls for each district.

### Pivot Table

```python
pd.pivot_table(df, values='Calls', index='District', columns='Month')
```

This allows comparison of monthly ambulance calls across districts.

---

# 8. Key Findings and Insights

From the analysis, the project aims to discover:

* Districts with the highest emergency call volumes
* Monthly patterns in ambulance calls
* Possible trends or seasonal changes in emergency demand

These insights may help understand how emergency services are used in different areas.

---

# 9. Project Timeline (5 Weeks)

| Week                     | Activities                                  |
| ------------------------ | ------------------------------------------- |
| Week 1 (06 Feb – 13 Feb) | Dataset search and project planning         |
| Week 2 (13 Feb – 20 Feb) | Data cleaning and preparation               |
| Week 3 (20 Feb – 06 Mar) | Data analysis and visualization             |
| Week 4 (06 Mar – 13 Mar) | Report writing and presentation preparation |

**Presentation Date:** 16 March

---

# 10. Outcome of the Project

Through this project, students will develop practical skills in data analytics.

**Skills Developed**

* Data cleaning and preprocessing
* Data analysis using Pandas
* Identifying trends and patterns in data
* Interpreting analytical results

---

# 11. Conclusion

This project demonstrates how data analytics techniques can be applied to emergency service data. By analyzing monthly ambulance calls, the team aims to identify patterns and trends that could help improve understanding of emergency service demand.

---

# 12. References

* Kaggle Dataset Repository
* Pandas Official Documentation
* Python Data Analysis Tutorials

---

# 13. Appendix

The appendix may include:

* Important Python code snippets
* Additional graphs and charts
* Tables generated during analysis

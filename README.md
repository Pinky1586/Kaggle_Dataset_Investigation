Investigate a Dataset: No-Show Medical Appointments

Author: Christina Jernberg

📌 Project Overview

This project analyzes over 110,000 medical appointments in Brazil to understand factors associated with patient no-shows. Missed medical appointments create financial strain for healthcare systems and reduce access to care. The goal of this analysis is to identify demographic, behavioral, and health-related patterns that may influence attendance.

The dataset includes patient demographics, medical conditions, SMS reminder status, welfare program enrollment, and appointment scheduling details.

📊 Dataset Summary

110,527 appointments

62,299 unique patients

14 variables

Overall no-show rate: ~20.2%

Key Variables

gender

age

neighbourhood

scholarship (Brazilian welfare program enrollment)

hipertension

diabetes

alcoholism

handcap (0–4 categories)

sms_received

no_show (target variable)

No missing values were present. Some data cleaning was required to correct datatypes and standardize column names.

🔧 Data Preparation

Data wrangling steps included:

Converting date fields to datetime

Converting binary indicators to boolean

Mapping "Yes"/"No" values to boolean for modeling

Standardizing column names (lowercase, underscores)

Creating age groups:

0–14

15–24

25–44

45–64

65+

Additional patient-level aggregations were created to analyze repeated no-show behavior.

🔍 Research Questions

How do gender, age, medical conditions, scholarship status, and SMS reminders affect no-show rates?

Among patients with multiple appointments, what proportion repeatedly no-show?

Are habitual no-shows associated with SMS reminders?

Do neighborhood-level patterns reveal meaningful differences?

📈 Key Findings
Age is the strongest predictor

Highest no-show rates occur between ages 15–24 (~25%)

Rates decline steadily after age 25

Slight increase again after age 80

Gender differences are minimal

Female no-show rate: 20.3%

Male no-show rate: 19.9%

Medical conditions

Hypertension and diabetes generally follow overall population trends

Alcoholism is associated with consistently higher no-show rates

Scholarship status

Patients receiving welfare support show slightly higher no-show rates across most age groups

SMS reminders

Patients who received SMS reminders showed higher no-show rates

Likely reflects targeted reminder strategy, not SMS causing absence

Repeated No-Shows

5.18% of patients missed 2+ appointments

60% of habitual no-show patients did not receive SMS reminders

📊 Visualizations

The project includes:

Line charts of no-show rate by age and gender

Neighborhood-level scatter plots

Condition-specific comparisons by age group

Multi-panel summary plots

Patient-level repeated no-show distribution analysis

All visualizations were built using matplotlib.

🛠 Tools Used

Python

Pandas

NumPy

Matplotlib

⚠️ Limitations

No geographic context beyond neighborhood labels

No socioeconomic data beyond scholarship indicator

SMS reminder assignment logic unknown

Handicap categories lack descriptive metadata

Because this is observational data, findings show association, not causation.

💡 Future Improvements

Apply logistic regression to quantify predictor strength

Include wait-time between scheduling and appointment

Explore temporal patterns (weekday effects)

Incorporate geospatial analysis if coordinates available

Model patient-level recurrence risk

📁 File Structure
Investigate_NoShow_Appointments/
│
├── noshowappointments-kagglev2-may-2016.csv
├── Investigate_NoShow_Appointments.ipynb
└── README.md

🎯 Project Objective

This project demonstrates structured data wrangling, feature engineering, exploratory data analysis, and patient-level behavioral pattern analysis. It highlights the ability to:

Clean and transform raw data

Engineer meaningful features

Identify behavioral patterns

Communicate findings visually

Interpret results with appropriate statistical caution

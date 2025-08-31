# Employee-Attrition-Analysis
Employee Attrition & Segmentation Analysis

This project provides a comprehensive analysis of employee attrition and workforce segmentation, helping HR and management identify trends, risks, and opportunities to improve retention and employee satisfaction.

Project Overview

The analysis covers 958 employees and includes dashboards for:

Employee Segmentation – evaluates demographics, engagement, satisfaction, training, and job roles.

Attrition Rate Analysis – examines attrition patterns from 2022–2024, highlighting risk factors such as OverTime, age, tenure, and engagement scores.

The project uses multiple Excel sheets to separate raw data, processed analysis, and dashboards for easier reporting and decision-making.

Key Insights
Employee Segmentation Dashboard

Total Employees: 958

% Female Employees: 52%

Average Age: 42 years

Average Engagement Score: 3.7 / 5

Average Satisfaction Score: 5.4 / 10

% OverTime Employees: 42%

Average Monthly Income: ₹93,517

% with High Training Level: 26%

Segmentation Findings:

Gender is fairly balanced; Engineering has higher female representation.

Managers earn the highest; Technicians and Consultants earn less.

High training correlates with high performance.

Low engagement + OverTime = retention risk.

Recommendations:

Expand training programs, especially for low-training segments.

Monitor and reduce OverTime workload.

Focus on development of Technicians and Executives.

Assess promotion equity.

Implement targeted engagement programs.

Attrition Rate Dashboard

Attrition Rate: 22%

Total Leavers: 206

Average Tenure of Leavers: 2.7 years

Average Income of Leavers: ₹94,273

Attrition Insights:

Highest attrition in Finance, Technicians, and young employees (22–24 years).

OverTime employees have higher attrition (24.9%) than non-OverTime (19.1%).

Medium engagement employees show unexpected higher attrition.

Recommendations:

Reassess workload for OverTime-heavy teams.

Improve retention strategies for junior employees.

Enhance satisfaction programs for highly engaged but at-risk employees.

Repository Structure
Employee-Attrition-Analysis/
│
├── data/
│   ├── raw/               # Original Excel file
│   ├── processed/         # Split Excel sheets (dashboards, analysis, reports)
│
├── scripts/
│   └── split_sheets.py    # Python script to split multi-sheet Excel into separate files
│
├── .gitignore
├── README.md
└── requirements.txt       # Python dependencies (pandas, openpyxl)

How to Use

Clone the repository:

git clone https://github.com/RAHULBAUNTHIYAL/Employee-Attrition-Analysis.git


Install dependencies:

pip install -r requirements.txt


Run the script to split Excel sheets (if needed):

python scripts/split_sheets.py

""import pandas as pd

# Replace with your Excel file name
input_file = "/content/HR Attrition Dashboard.xlsx"

# Load the Excel file
xls = pd.ExcelFile(input_file)

# Loop through each sheet and save as a new Excel file
for sheet_name in xls.sheet_names:
    df = pd.read_excel(input_file, sheet_name=sheet_name)
    output_file = f"{sheet_name}.xlsx"
    df.to_excel(output_file, index=False)
    print(f"Saved: {output_file}")
"" PLease copy paste this yourself this part


Explore the dashboards and processed data in data/processed/.



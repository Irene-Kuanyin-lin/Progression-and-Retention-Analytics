# Progression and Retention Analytics

## 📌 Project Overview

An analytics project examining student progression and attrition at Macquarie Business School. The project combines data preparation, interactive Power BI dashboards and logistic regression to identify curriculum bottlenecks and students who may benefit from early support.

Developed for **BUSA8031 – Business Analytics Project**, Macquarie University | 2025.

### Business Relevance

- **Course Directors:** Review high-failure units and progression barriers to inform course design.
- **Student support teams:** Identify at-risk cohorts for targeted outreach.
- **University management:** Use evidence to inform retention strategies and resource allocation.

## 🛠️ Tools & Methods

Power BI · Python/Jupyter Notebook · Data Cleaning · Feature Engineering · Exploratory Analysis · Logistic Regression

## 📂 Dataset

The project used de-identified undergraduate enrolment and retention data provided by Macquarie University's Business Intelligence and Reporting team.

- **Period:** 2020–2025.
- **Scope:** 284,656 unit enrolment records covering 21,814 students across 85 courses.
- **Features:** Grades, weighted average marks (WAM), credit points, study load, course progress, demographic attributes and retention indicators.

Source student data is not included with this README. Access and redistribution are subject to university permissions.

## 🔎 Project Workflow

### 1. Data Preparation & Feature Engineering

- Addressed missing values, checked data types and reviewed temporal consistency.
- Aggregated unit enrolments into student-level records for predictive modelling.
- Created features describing course progress, study duration, annual study load, failures, repeated failures and withdrawals.
- Encoded categorical variables and scaled numerical predictors where required.

### 2. Interactive Power BI Dashboards

**Dashboard 1 — Curriculum Barrier Analysis**

- Compared unit failure rates and total failure counts.
- Examined repeated failures and progression barriers across course levels.
- Used course and year filters to support cohort-specific exploration.
![Dashboard 1: Curriculum Barrier Analysis](Screenshot%20of%20Dashboard%201%20Curriculum%20Barrier%20Analysis.jpg)

**Dashboard 2 — Student Attrition and Risk Behaviour**

- Compared completion, retention and dropout patterns.
- Explored associations between attrition, study load, academic performance and demographic characteristics.
- Supported course-level comparison and identification of cohorts requiring further investigation.
![Dashboard 2: Student Attrition and Risk Behaviour](Screenshot%20of%20Dashboard%202%20Student%20Attrition%20and%20Risk%20Behaviour.jpg)

### 3. Predictive Modelling

- Developed a logistic regression model to estimate student dropout risk.
- Used five predictors: WAM, course progress, failure count, repeat-failure count and withdrawal count.
- Split labelled records into 70% training and 30% testing subsets.
- Evaluated accuracy and ROC AUC, then generated risk scores for active students in 2025.

## 📊 Results & Key Findings

| Area | Reported finding |
| --- | --- |
| Curriculum barriers | Foundation units concentrated high failure counts and repeated failures. |
| Academic performance | Lower WAM, limited progress and repeated failures were associated with attrition. |
| Study load | Very low study loads, particularly among part-time students, were associated with greater attrition. |
| Model performance | Approximately **86% test accuracy** and **0.90 ROC AUC**. |
| Risk scoring | **285 of 7,079 active students** received predicted dropout probabilities above 80%. |

These are historical associations and model estimates. Risk scores identify candidates for further review; they are not confirmed future dropouts.

## 💡 Recommendations

- Review high-risk foundation units, including assessment structure, workload and sequencing.
- Strengthen first-year transition support through peer mentoring and clearer guidance on university services.
- Use tiered support strategies to prioritise outreach while continuing preventive support for lower-risk students.

The project proposed these actions; it did not measure the effect of implemented interventions on retention.

## 📝 Limitations & Future Improvements

- Behavioural factors such as motivation, engagement and external commitments were not fully captured.
- Missing data and the use of a single model limit the analysis.
- A temporal holdout would better assess performance when predicting a future cohort.
- Further validation should examine precision, recall, probability calibration and performance across student groups before operational use.

## 📂 Project Materials

The client report documents [View the Full Client Report (PDF)](BUSA8031%20Client%20Report.pdf) two Power BI dashboards and a data-preparation/predictive-modelling notebook. This README is based on the report; the underlying code and dashboard files have not been independently executed or validated here.

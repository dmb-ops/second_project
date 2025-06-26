# 📊 Vanguard’s UI Redesign Analysis

## 🎯 Project Objective

As Vanguard’s clients adapt to a fast-changing digital environment, the company rolled out a new, more intuitive interface (UI) with in-context prompts. This project investigates whether those design changes led to **higher application completion rates** through an A/B testing approach.

---

## 🧩 Dataset Overview

We worked with three main datasets:

- **Client Profiles:** Demographics, education level, income, tenure, etc.
- **Digital Footprints:** User online interactions, divided into pt_1 and pt_2.
- **Experiment Roster:** Identifies users belonging to either Control or Test groups.

---

## 🧹 Data Cleaning & Wrangling

- Removed duplicates and unnecessary columns (`visitor_id`, `visit_id`, `clnt_tenure_mnth`).
- Filled in missing values and corrected inconsistent formats.
- Merged datasets to create a unified DataFrame for comprehensive analysis.

---

## 📊 Exploratory Data Analysis (EDA)

### Key Questions Explored:

- Who are the primary users of the online process in terms of age and tenure?
- How are gender and age distributed across Test and Control groups?

### Notable Findings:

- **Average client age:** 46.4 years  
- **Most frequent age:** 58.5 years  
- Majority of users are middle-aged to older, confirming a mature digital client base.

---

## 📈 Performance Metrics & KPIs

- Created contingency tables to validate group randomization across gender.
- Verified **statistically balanced Control and Test groups**, with a negligible discrepancy in gender label 'X'.

These checks confirmed **reliable comparisons** of completion rate KPIs across groups.

---

## 🧪 Hypothesis Testing

### Test: Average Age Difference

- **Objective:** Check if age distribution differs between Test and Control.
- **Method:** Independent t-test using `ttest_ind()`.
- **Result:** p-value = **4.77e-15** → significant age difference detected.
  
➡️ Indicates **imperfect randomization**, as the Test group had a younger average age.

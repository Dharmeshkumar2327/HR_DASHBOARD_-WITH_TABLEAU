# 📊 HR Analytics Dashboard — Tableau

## 📌 Project Overview

The **HR Analytics Dashboard** is an interactive Tableau project designed to analyze and visualize employee data. The dashboard provides insights into workforce demographics, hiring and termination trends, employee salaries, education levels, job roles, departments, performance ratings, and geographic distribution.

The project transforms raw HR data into interactive visualizations and KPIs that help users understand workforce patterns and make data-driven HR decisions.

---

## 🎯 Project Objectives

* Analyze the overall employee workforce.
* Track hiring and termination trends over time.
* Understand employee demographics and age distribution.
* Analyze salary distribution across employees and job roles.
* Compare education levels with employee performance.
* Analyze workforce distribution by department and job title.
* Explore employee distribution by state and city.
* Identify active and terminated employees.
* Provide detailed employee-level information through an interactive dashboard.

---

## 🛠️ Tools & Technologies

* **Tableau** – Data visualization and dashboard development
* **CSV** – Source data
* **Tableau Calculations** – KPI and analytical calculations
* **Tableau Filters** – Interactive data exploration

---

## 📂 Dataset

The project uses a **Human Resources dataset** containing employee information such as:

* Employee ID
* First Name
* Last Name
* Gender
* State
* City
* Education Level
* Birthdate
* Hire Date
* Termination Date
* Department
* Job Title
* Salary
* Performance Rating

---

## 📊 Dashboard Features

### 👥 Workforce Analysis

The dashboard provides KPIs for:

* Total Employees
* Total Hired Employees
* Total Active Employees
* Total Terminated Employees

Employee status is calculated based on the termination date.

```text
If Termination Date is NULL → Hired / Active
If Termination Date exists → Terminated
```

---

### 📈 Hiring & Termination Trends

The dashboard analyzes employee hiring and termination patterns over time.

Visualizations include:

* Hired Employees by Year
* Terminated Employees by Year
* Workforce Status
* Hiring and termination trends

These visualizations help identify changes in workforce size over different periods.

---

### 🎓 Education Analysis

The dashboard analyzes employee education levels and their relationship with other HR metrics.

Examples include:

* Education Level distribution
* Education vs Performance
* Gender vs Education Level
* Age vs Education

---

### 💰 Salary Analysis

Salary-related analysis includes:

* Salary distribution
* Age vs Salary
* Salary comparison across employees
* Salary analysis by job-related dimensions

This helps identify salary patterns within the workforce.

---

### 👨‍💼 Job & Department Analysis

The dashboard provides employee distribution by:

* Department
* Job Title
* Job Role
* Employee Status

Users can use interactive filters to explore specific departments or job titles.

---

### 🌎 Geographic Analysis

Employee locations are analyzed using:

* State
* City
* Location
* Geographic distribution

The dashboard also categorizes locations into **HQ** and **Branch** based on the state information.

---

## 🧮 Tableau Calculated Fields

Several calculated fields are used to enhance the analysis.

### Employee Status

```text
IF ISNULL([Termdate]) THEN 'Hired'
ELSE 'Terminated'
END
```

### Total Employees

```text
COUNT([Employee_ID])
```

### Total Terminated

```text
COUNT(
    IF NOT ISNULL([Termdate])
    THEN [Employee_ID]
    END
)
```

### Total Active

```text
COUNT(
    IF ISNULL([Termdate])
    THEN [Employee_ID]
    END
)
```

### Employee Age

```text
DATEDIFF('year', [Birthdate], TODAY())
```

### Full Name

```text
[First Name] + ' ' + [Last Name]
```

### Length of Hire

```text
IF ISNULL([Termdate])
THEN DATEDIFF('year', [Hiredate], TODAY())
ELSE DATEDIFF('year', [Hiredate], [Termdate])
END
```

### Age Groups

Employees are categorized into different age groups such as:

* Under 25
* 25–34
* 35–44
* 45–54
* 55+

---

## 📑 Dashboard Worksheets

The Tableau workbook contains multiple analytical worksheets, including:

* Age
* Age Groups
* Age vs Education
* Age vs Salary
* Active Employees
* Hired Employees
* Terminated Employees
* Cities
* Departments
* Detailed Employee Data
* Education Levels
* Education vs Performance
* Gender
* Gender vs Education Level
* Hired by Year
* Job Titles
* Location
* States
* Terminated by Year

---

## 🔍 Key Business Questions

The dashboard helps answer questions such as:

1. How many employees are currently active?
2. How many employees have been hired?
3. How many employees have been terminated?
4. What are the hiring trends over the years?
5. Which departments have the highest number of employees?
6. Which job titles are most common?
7. What is the employee age distribution?
8. How are employees distributed across education levels?
9. How does education level relate to performance?
10. How are salaries distributed across employees?
11. Which states and cities have the highest employee concentration?
12. What is the distribution of employees by gender?
13. How long do employees typically stay with the organization?

---


---

## 🚀 How to Open the Project

1. Download or clone this repository.

```bash
git clone https://github.com/your-username/HR-Analytics-Tableau.git
```

2. Open **Tableau Desktop**.

3. Open:

```text
HR Dashboard.twbx
```

4. Explore the dashboard using the available filters and interactive visualizations.

---

## 📸 Dashboard Preview

Add your Tableau dashboard screenshot here:

```markdown
![HR Dashboard](Dashboard/HR%20Dashboard%20Screenshot.png)
```

---

## 💡 Skills Demonstrated

This project demonstrates practical skills in:

* Tableau Dashboard Development
* Data Visualization
* Data Analysis
* HR Analytics
* KPI Development
* Calculated Fields
* Interactive Filters
* Workforce Analysis
* Employee Demographic Analysis
* Salary Analysis
* Trend Analysis
* Geographic Analysis
* Business Intelligence

---

## 📌 Project Type

**Data Analytics | Business Intelligence | HR Analytics | Tableau**

---

## 👨‍💻 Author

**Dharmesh Kumar**

Data Analyst | Tableau | Power BI | SQL | Python

---


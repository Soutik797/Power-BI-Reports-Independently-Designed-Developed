# Power-BI-Reports-Independently-Designed-Developed


I independently created powerful and interactive Power BI reports to visualize and analyze business-critical data. These dashboards were developed entirely based on my knowledge of data modeling, DAX, and best practices in visualization design.

The goal of each report was to uncover meaningful patterns, track performance metrics, and support strategic decisions. By applying advanced analytical techniques and focusing on visual storytelling, I delivered clean, user-friendly, and scalable dashboards — all without relying on external tools or support.


✅ Key Highlights

🔧 Self-Driven Development
Designed and built Power BI reports independently, showcasing a strong command of data analytics principles.

🧠 Expertise in Data Modeling & DAX
Applied advanced understanding of data relationships, measures, and DAX formulas to develop efficient data models.

📈 Interactive Dashboards
Created dynamic visuals using slicers, filters, KPI indicators, and drill-down functionalities for in-depth data analysis.

🧩 Visual Storytelling
Focused on crafting visuals that clearly communicate trends, comparisons, and actionable insights.

🚀 Scalable & Clean Design
Ensured every report was easy to navigate, visually appealing, and aligned with user needs and business goals.

💡 Independent Problem Solving
Demonstrated the ability to troubleshoot issues, optimize performance, and enhance visuals — all through self-guided learning.







➡️ HR ANALYTICS DASHBOARD

<img width="600" alt="B" src="https://github.com/user-attachments/assets/3a25ad52-467d-4abd-90aa-9af4de23ca5a" />



# 📊 HR Analytics Dashboard Overview

## 📝 Summary

The HR Analytics Dashboard provides a comprehensive view of employee attrition trends across demographics, job roles, and organizational segments. Out of 1,470 employees, 237 have left the organization, reflecting an attrition rate of 16.1%. Key findings include high attrition among the 26–35 age group, a concentration in the Life Sciences education field, and most attrition occurring among employees earning below 5K. Males account for the majority of attrition cases. Despite this, job satisfaction scores tend to cluster around moderate to high levels, offering important insights into engagement and retention strategies.

---

## 📈 Key Metrics

| Metric                    | Value       |
|--------------------------|-------------|
| Total Employees          | 1,470       |
| Attrition Count          | 237         |
| Attrition Rate           | 16.1%       |
| Average Age              | 37          |
| Average Salary           | 6.5K        |
| Average Years at Company | 7.0         |

---

## 📊 Analysis by Dimension

### ➤ Attrition by Age Group
- 26–35: **116**
- 18–25: 44
- 36–45: 43
- 46–55: 26
- 55+: 8

### ➤ Attrition by Gender
- Male: **150**
- Female: 87

### ➤ Attrition by Education Field
- Life Sciences: **38%**
- Medical: 27%
- Marketing: 15%
- Technical Degree: 14%
- Other: 5%

### ➤ Attrition by Salary Slab
- Upto 5K: **163**
- 5K–10K: 49
- 10K–15K: 20
- 15K+: 5

### ➤ Attrition by Job Role (Top 4)
- Laboratory Technician: **62**
- Sales Executive: 57
- Research Scientist: 47
- Sales Representative: 33

### ➤ Attrition by Years at Company
- Highest attrition within **first few years** of tenure, especially in entry/mid-level roles.

---

## 😀 Job Satisfaction Breakdown

| Job Role                  | Total Attrition | Satisfaction (1–4) |
|---------------------------|------------------|---------------------|
| Laboratory Technician     | 62               | Mixed (Mostly 3–4)  |
| Sales Executive           | 57               | Mixed (2–4)         |
| Research Scientist        | 47               | Mixed (1–4)         |
| Sales Representative      | 33               | Mixed (1–3)         |

---

## 💡 Visual Insights

- 📌 **26–35 age group** has the highest attrition.
- 📌 **Male employees** account for ~63% of attrition.
- 📌 Employees earning **<5K** dominate attrition.
- 📌 **Life Sciences** background employees see the highest attrition.
- 📌 **Sales and Technical roles** need focused retention strategies.

---


---

## 🧮 DAX / Calculated Columns (Suggested)

```DAX
-- Attrition Rate
Attrition Rate = DIVIDE(COUNT(HR_Analytics[Attrition]), COUNT(HR_Analytics[EmployeeID]))

-- Average Salary
Average Salary = AVERAGE(HR_Analytics[MonthlyIncome])

-- Salary Slab
Salary Slab = SWITCH(TRUE(),
    HR_Analytics[MonthlyIncome] <= 5000, "Upto 5k",
    HR_Analytics[MonthlyIncome] <= 10000, "5k–10k",
    HR_Analytics[MonthlyIncome] <= 15000, "10k–15k",
    "15k+"
)

-- Attrition by Role
Attrition by Role = CALCULATE(COUNT(HR_Analytics[EmployeeID]), HR_Analytics[Attrition] = "Yes")

---

<!-- SPACE -->
###   <!-- empty heading or any text creates a gap -->
<br><br><br>  <!-- This creates vertical space -->




➡️ SuperStore - Sales Dashboard

<img width="602" alt="A" src="https://github.com/user-attachments/assets/c356f8dd-1c98-4bcd-b14f-f4b871a27927" />



# 🛒 Super Store Sales Dashboard – Power BI Report

## 🛑 Overview

The **Super Store Sales Dashboard** in Power BI delivers a comprehensive analysis of sales performance across various business dimensions such as **product categories, customer segments, payment and ship modes, sub-categories, time, and geography**. 

### 📌 Key Performance Indicators (KPIs)
- **Total Sales**: 450.23K  
- **Total Quantity**: 6,251  
- **Total Profit**: 53K  
- **Average Delivery Days**: 4  

Visual elements like **donut charts, bar charts, line graphs, cards, slicers, and maps** offer in-depth insights into trends by **region, state, time (YOY for 2019 & 2020)**, and **customer behavior**. Dynamic filtering enables focused analysis by region (**Central, East, South, West**) to assist in **data-driven decision-making**.

---

## ✅ 1. Type of Analysis Performed

The dashboard focuses on performance analytics for a retail Super Store across key dimensions:

- 📆 **Time-based Trends** (Monthly YOY)
- 🌍 **Geographical Insights** (Region & State)
- 👤 **Customer Segmentation**
- 📦 **Product Category/Sub-Category**
- 🚚 **Shipping and Payment Modes**

---

## ✅ 2. Visualizations Used

| Visualization Type     | Purpose                                             |
|------------------------|-----------------------------------------------------|
| 📇 **Card**             | Displays key KPIs like Sales, Profit, Quantity      |
| 🍩 **Donut Chart**      | Shows proportional breakdowns (e.g., by Payment Mode) |
| 📊 **Clustered Bar**    | Compares values across categories and sub-categories |
| 🌄 **Stacked Area Chart**| Shows Monthly Profit/Sales YoY                     |
| 🎛 **Slicers**          | Filter views by Region, Category, etc.              |
| 🗺 **Map**               | Displays sales distribution across states/regions   |

---

## 📊 Dataset-Based Analysis

Breakdown of key insights derived from the dataset:

- **Total Sales**: 450.23K
- **Total Quantity Sold**: 6,251
- **Total Profit**: 53K
- **Average Delivery Days**: 4
- **Sales by Payment Mode**: Insightful split by payment preferences
- **Sales by Category & Sub-Category**: Identify top-performing products
- **Sales by Ship Mode**: Optimize logistics strategies
- **Segment-Wise Sales**: Analyze customer behavior and value
- **Monthly Profit/Sales YOY (2019–2020)**: Track seasonal and annual trends

---

## 🧮 DAX Measures (KPI Formulas)

```DAX
-- Total Sales
Total Sales = SUM('SuperStore_Sales_Dataset'[Sales])

-- Total Quantity
Total Quantity = SUM('SuperStore_Sales_Dataset'[Quantity])

-- Total Profit
Total Profit = SUM('SuperStore_Sales_Dataset'[Profit])

-- Average Delivery Days
Avg Delivery = AVERAGE('SuperStore_Sales_Dataset'[AvgDelivery])














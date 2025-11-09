# 💼 HR Analytics Dashboard | Power BI

## 📘 Project Overview
The **HR Analytics Dashboard** is an interactive business intelligence solution built in **Microsoft Power BI**.  
It provides a comprehensive view of employee data to help HR departments understand **attrition trends**, **demographics**, and **key workforce metrics** that drive better employee retention and decision-making.

---

## 🎯 Objective
The main goal of this project is to identify and analyze the **factors influencing employee attrition** in an organization.  
By using data visualization and DAX-based insights, this dashboard enables HR managers to take **data-driven decisions** on talent management, hiring, and employee engagement.

---

## 📊 Key Insights
- 👥 **Total Employees:** 1470  
- 🚪 **Employees Left (Attrition):** 237  
- 📉 **Attrition Rate:** 16%  
- 🎂 **Average Age:** 37 years  
- 💰 **Average Salary:** 6.5K  
- ⏱ **Average Tenure:** 7 years  

These KPIs help identify workforce stability, employee demographics, and turnover rates at a glance.

---

## 🧩 Dashboard Features
- Interactive and filterable dashboard with department and gender filters.  
- Dynamic KPIs for:
  - Count of Employees  
  - Attrition Count  
  - Attrition Rate  
  - Average Age, Salary, and Tenure  
- Visual breakdowns:
  - **Attrition by Education Field**
  - **Attrition by Age Group**
  - **Attrition by Job Role**
  - **Attrition by Salary Slab**
- Dark gradient professional theme with consistent formatting.
- Real-time insights using **DAX measures** and Power Query transformations.

---

## 🧮 DAX Measures Used

```DAX
CountOfEmployee =
COUNTROWS(HR_Analytics)

AttritionCount =
COUNTROWS(
    FILTER(HR_Analytics, HR_Analytics[Attrition] = "Yes")
)

AttritionRate =
DIVIDE(
    COUNTROWS(FILTER(HR_Analytics, HR_Analytics[Attrition] = "Yes")),
    COUNTROWS(HR_Analytics),
    0
)

# Databel Telecom Customer Churn Analysis

An interactive **Power BI** analytics dashboard evaluating customer churn metrics, demographic behavior, geographic distribution, and churn drivers for the Databel dataset.

---

## 📊 Project Overview & Key Insights

* **Total Customers:** 7,000
* **Churned Customers:** 1,796
* **Overall Churn Rate:** 27%
* **Total Revenue/Charge:** $7.0M
* **Average Customer Age:** 47.45 years

### Primary Findings
1. **Top Drivers of Churn:** Competitor actions (better offers/hardware) and customer support attitudes account for the highest proportion of lost customers.
2. **Contract Analysis:** Monthly contract holders experience significantly higher churn (~40%–47%) compared to yearly contract holders (6%–7%).
3. **Customer Support Escalation:** Churn rate spikes dramatically after 3 or more customer service calls, reaching up to 100% for customers with 4+ interactions.
4. **Group Plans:** Single-user accounts exhibit a higher churn rate (33%) with higher average monthly charges ($33) compared to grouped accounts ($23/month, ~6%-8% churn).

---
<img width="950" height="646" alt="Screenshot 2026-08-08 154418" src="https://github.com/user-attachments/assets/fbdd4fcc-e079-4171-8b67-bfe5f286c9c4" />

---


## 🛠️ Tools & Technologies Used
* **Business Intelligence:** Microsoft Power BI Desktop
* **Data Transformation:** Power Query
* **Data Modeling & Calculations:** DAX (Data Analysis Expressions)
* **Visualization Assets:** Custom dark theme layout, Bing Maps visual, custom gauges, combo bar/line charts

---

## 📈 Dashboard Features & Architecture

* **KPI Cards & Gauges:** Real-time visibility into overall churn rate (27%), revenue lost, total customer volume, and average age.
* **Geographic Analysis:** US State Map visual mapping regional churn concentration.
* **Root-Cause Breakdowns:**
  * Horizontal bar chart detailing top 10 churn reasons (Competitor competitor matrix, support attitude, pricing, etc.).
  * High-level churn categories breakdown (Competitor, Attitude, Dissatisfaction, Price).
* **Demographic & Behavior Segmentation:**
  * Clustered column chart comparing churn rates across contract types (Monthly vs. Yearly) split by gender.
  * Area line graph tracking churn probability relative to customer service contact count.
  * Age binning combo chart illustrating customer volume alongside churn rate trends by age brackets.

---

## 📂 Data Transformation Process (Power Query & DAX)

1. **Data Cleaning & Prep:**
   * Handled missing values and standardized demographic variables (Gender, State, Age).
   * Grouped customer ages into discrete brackets/bins for age-based cohort analysis.
2. **DAX Measures:**
   ```dax
   Total Customers = COUNT(Databel[CustomerID])

# Colgate-Palmolive-Project

# 📈 Enhancing Toothbrush Manufacturing Throughput

## FOCUS: Data-Driven Analysis of Downtime and Quality Control

---

## 1. Project Overview

This project analyzes **one year of production and machine data** from a primary toothbrush manufacturing facility operated by **Colgate-Palmolive**. The objective is to identify operational inefficiencies related to **machine downtime** and **product defects**, quantify their business impact, and propose **data-driven strategies** to improve overall manufacturing throughput.

Machine downtime and quality issues are known to cause significant financial losses. This project provides a structured analytical approach to determine:

* Where losses occur
* Why they occur
* Which improvement initiatives yield the highest return

---

## 2. Business Objectives

The analysis addresses three core business questions:

### 2.1 Performance Overview

Provide a comprehensive view of factory performance using key manufacturing metrics:

* **Overall Equipment Effectiveness (OEE)**
* **Defect Rate**
* **Production Throughput Yield**

### 2.2 Root Cause Analysis

Identify primary drivers of machine downtime and product defects, focusing on:

* Specific machines or production lines
* Work shifts
* Product types

Issues are further classified into:

* **Systemic issues** (recurring and process-related)
* **Emerging issues** (infrequent but high-risk)

### 2.3 Impact Quantification and Recommendations

* Quantify direct and indirect business impacts of downtime and defects
* Propose actionable, data-driven improvement strategies

---

## 3. Dataset Description

### 3.1 Data Sources

The analysis uses three CSV files:

* **production_log.csv** – Daily production output, good units, and defects
* **maintenance_order.csv** – Maintenance activities and downtime records
* **cross_reference.csv** – Mapping between machines, production lines, and products

### 3.2 Data Characteristics

* **Time horizon:** 1 full year
* **Categorical variables:** `LINE_NAME`, `UTIL_REASON_DESCRIPTION`, `SHIFT`, `PRODUCT_TYPE`
* **Numerical variables:** `DOWNTIME`, `GOOD_PRODUCTION_QTY`, `DEFECT_QTY`

### 3.3 Data Integration & Cleaning

* Joined datasets using reference keys in `cross_reference.csv`
* Handled missing values
* Standardized categorical values
* Validated production and downtime ranges

---

## 4. Methodology

### 4.1 Exploratory Data Analysis (EDA)

EDA is conducted to:

* Understand downtime and defect distributions
* Identify time-based trends
* Compare performance across machines, lines, and shifts

### 4.2 Key Metrics Definition

**Overall Equipment Effectiveness (OEE)**

```
OEE = Availability × Performance × Quality
```

**Defect Rate**

```
Defect Rate = Defective Units / Total Produced Units
```

**Production Throughput Yield**

```
Throughput Yield = Good Units / Total Input Units
```

### 4.3 Root Cause Categorization

Downtime and defects are analyzed by:

* Cause type (mechanical, operational, maintenance-related)
* Frequency and duration
* Impact magnitude

A **Pareto (80/20) analysis** is applied to prioritize the most critical issues.

---

## 5. Performance Overview (Question 1)

A performance dashboard summarizes:

* Average OEE across production lines
* Overall defect rate
* Average throughput yield

**Key insights include:**

* Underperforming lines and machines
* Periods of reduced efficiency
* Performance variability across shifts

---

## 6. Root Cause Analysis (Question 2)

The analysis identifies:

* Most frequent and impactful downtime causes
* Machines and lines responsible for the majority of lost production time
* Product types and shifts associated with higher defect rates

Issues are classified as:

* **Systemic issues:** recurring, process-related problems
* **Emerging issues:** rare but potentially high-impact risks

---

## 7. Business Impact Quantification (Question 3)

### 7.1 Direct Losses

* Total production units lost due to downtime
* Total defective units resulting in material waste

### 7.2 Indirect Losses (Assumption-Based)

Estimated impacts include:

* Missed delivery targets
* Reduced customer satisfaction
* Increased operational pressure during recovery periods

---

## 8. Key Insights

* A small number of downtime causes account for the majority of lost production time
* Specific machines consistently act as bottlenecks
* Defects are concentrated in limited product types and production conditions

---

## 9. Data-Driven Recommendations

### Strategy 1 – Predictive Maintenance

Focus maintenance efforts on machines with recurring downtime patterns using historical failure data to reduce unplanned stoppages.

### Strategy 2 – Quality Control Optimization

Enhance quality checks for high-defect product types and standardize best practices from top-performing production lines.

### Strategy 3 – Operational and Shift Optimization

Improve operator training and staffing allocation for shifts associated with higher downtime and defect frequency.

---

## 10. Assumptions and Limitations

### Assumptions

* Production demand is sufficient to absorb additional output
* Each defective unit represents a direct material loss

### Limitations

* No direct cost data for downtime or defects
* Customer-level impact is estimated, not directly measured

---

## 11. Technology Stack

* **Python:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn, Power BI (optional)
* **Environment:** Jupyter Notebook

---

## 12. Repository Structure

```
├── data/
│   ├── production_log.csv
│   ├── maintenance_order.csv
│   └── cross_reference.csv
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Root_Cause_Analysis.ipynb
│   └── 03_Impact_Quantification.ipynb
├── dashboard/
│   └── performance_dashboard.pbix
├── README.md
```

---

## 13. Conclusion

This project demonstrates how manufacturing data can be leveraged to uncover operational bottlenecks, quantify business losses, and support data-driven decision-making. The insights and recommendations provide a strong foundation for improving machine uptime, reducing waste, and increasing overall production throughput.

**Future work** may extend this analysis into predictive maintenance modeling and real-time pe

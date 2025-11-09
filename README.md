# 📊 Bank Marketing Data Analysis (Python Project)

## 🧭 Project Overview
This project analyzes a **bank marketing dataset** to understand which customer groups are most likely to subscribe to a term deposit.  
The focus is on **data analysis** (not machine learning) — using Python for cleaning, exploration, feature engineering, and deriving business insights.

**Goal:** Identify patterns and actionable recommendations to improve the effectiveness of future marketing campaigns.

---

## 🧰 Tools & Libraries
- **Python**
- **Pandas** – data manipulation  
- **Matplotlib** – data visualization  
- **NumPy** – numerical operations  

---

## 🧩 Dataset
The dataset contains marketing campaign data from a bank, with details such as:
- Customer demographics (`age`, `job`, `education`, `marital`)
- Financial information (`balance`, `loan`, `housing`)
- Campaign details (`contact`, `duration`, `campaign`, `pdays`, `previous`)
- Response variable (`deposit`: whether the client subscribed to a term deposit)

---

## 🔄 Project Workflow

### **Step 1: Data Ingestion & Inspection**
- Loaded the dataset using `pandas.read_csv()`
- Inspected column names, missing values, and data types
- Verified dataset shape and structure

### **Step 2: Data Cleaning**
- Removed trailing characters (e.g., “.”) and standardized text formatting  
- Replaced missing values and handled special codes (`pdays = -1` → “not previously contacted”)
- Converted `deposit` to binary form (1 = yes, 0 = no)

### **Step 3: Handling Special Columns**
- Added a `not_previously_contacted` flag based on `pdays`
- Ensured categorical values were consistent and meaningful

### **Step 4: Exploratory Data Analysis (EDA)**
- Summary statistics and visual exploration  
- Identified distributions and outliers for numeric variables  
- Visualized categorical features with bar charts

### **Step 5: Feature Engineering**
- Created new useful columns:
  - `age_group`: 18–30, 31–50, 51+  
  - `any_loan_flag`: 1 if housing or personal loan present  
  - `high_contact_flag`: 1 if contacted > 3 times  
  - `recent_contact_flag`: 1 if contacted within 7 days

### **Step 6: Descriptive & Comparative Analysis**
- Conversion rate analysis by:
  - Job type, education level, marital status, loan status, and age group  
- Correlation analysis to measure relationships between numeric features and deposit outcome  
- Visualization of conversion trends using bar charts

### **Step 7: Insights & Recommendations**
**Overall Conversion Rate:** **47.38 %**

#### Top Performing Segments
| Segment | Insight |
|----------|----------|
| **Job** | Students (74.7%) and retirees (66.3%) are most likely to subscribe |
| **Education** | Higher education (tertiary – 54.1%) links to better conversion |
| **Marital Status** | Singles (54.4%) respond better than married clients |
| **Loan Flag** | Clients without loans convert more (59.6%) than those with loans (36.5%) |
| **Age Group** | Young adults (18–30) and older clients (51+) respond better |
| **Numeric Drivers** | Call duration has strongest correlation (r = 0.45) with deposit outcome |

#### Key Takeaways
1. Focus future campaigns on students, retirees, and highly educated individuals.  
2. Target customers with no existing loans and higher balances.  
3. Optimize outreach strategy — fewer, longer-quality calls perform better than frequent short ones.  
4. Personalize messaging for younger (growth-focused) and older (security-focused) audiences.  

---

## 📈 Example Visualizations
- Conversion rate by job category  
- Conversion rate by education level  
- Correlation of numeric features with `deposit`

*(See notebook for detailed charts)*

---

## 💡 Conclusion
The analysis highlights clear customer segments with high conversion potential.  
By refining targeting and communication strategies, the bank could significantly improve success beyond the current **47 %** conversion rate.

---

## 📁 Repository Structure

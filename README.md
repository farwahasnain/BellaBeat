# 📊 BellaBeat Wellness Data Analysis (EDA)

## 📌 Project Overview
This project explores user behavior patterns using the **BellaBeat Fitbit dataset**, with a focus on three core dimensions of wellness:

- **Daily Activity** (steps, calories burned)
- **Sleep Behavior** (sleep duration)
- **Weight Trends** (weight and BMI)

The objective of this analysis is to identify behavioral patterns and relationships across these dimensions and translate data insights into **actionable product recommendations** for a wellness-focused wearable platform like BellaBeat.

---

## 📂 Datasets Used

The analysis is based on the following cleaned datasets:

- `Cleaned_Daily.Activity.csv`
- `Cleaned_Sleep.Day.csv`
- `Cleaned_Weight.Log.csv`

These datasets were merged to enable cross-feature analysis while accounting for differences in data coverage.

---

## 🧹 Data Preparation

- Standardized column names and date formats across datasets
- Merged datasets using `customer_id` and `date`
- Created:
  - `df_merged`: master dataset containing activity, sleep, and weight data
  - `df_sleep_analysis`: subset containing only records with valid sleep data
- Missing sleep and weight records were treated as **behavioral gaps**, not data quality issues

---

## 📈 Exploratory Data Analysis & Key Findings

---

## 1️⃣ Activity Analysis (Steps & Calories)

### Findings
- Daily activity data has the highest record count, indicating consistent device usage for movement tracking.
- A **moderate positive correlation (r = 0.41)** exists between steps taken and calories burned.
- Average step counts vary by day of the week:
  - **Tuesdays show the highest average step counts**
  - **Saturdays follow as the second-highest**
  - **Sundays record the lowest average step counts**

### Conclusion
Steps are a strong driver of calorie burn and serve as a reliable indicator of daily activity levels. Weekly activity patterns suggest both structured weekday movement and higher discretionary activity on weekends, with reduced activity on Sundays.

---

## 2️⃣ Sleep Analysis

### Findings
- Sleep data coverage is significantly lower than activity data, indicating inconsistent sleep tracking among users.
- Correlation analysis shows:
  - **No meaningful relationship between sleep duration and calories burned (r = −0.03)**
  - **A weak negative correlation between sleep duration and steps taken (r = −0.19)**
- Sleep behavior appears largely independent of daily activity intensity.

### Conclusion
Sleep duration does not directly influence calorie expenditure or step count. Instead, sleep supports recovery and overall well-being, functioning as a complementary—but distinct—pillar of wellness alongside physical activity.

---

## 3️⃣ Weight Analysis

### Findings
- Weight data has the lowest coverage, reflecting the more manual and less frequent nature of weight logging.
- Weight and BMI values remain relatively stable over short time periods.
- No strong short-term relationship is observed between daily activity or sleep and immediate changes in weight.

### Conclusion
Weight trends reflect long-term lifestyle patterns rather than day-to-day behaviors. Weight metrics are best used for longitudinal progress tracking rather than daily performance evaluation.

---

## 🔗 Cross-Dataset Insights

- **Steps** are closely linked to calorie burn and are a key driver of physical activity outcomes.
- **Sleep** primarily supports recovery and wellness rather than energy expenditure.
- **Weight** reflects long-term behavioral consistency rather than short-term fluctuations.

These findings reinforce the importance of treating activity, sleep, and weight as **distinct but interconnected dimensions of wellness**.

---

## 💡 Product Recommendations

Based on the analysis:

- Maintain **step-based goals** as the core driver of calorie and activity features
- Frame sleep insights around **recovery, consistency, and overall well-being**, rather than calorie burn
- Introduce **recovery-aware activity recommendations** on days following longer or shorter sleep
- Encourage sleep and weight tracking using **trend-based insights** instead of daily performance comparisons
- Segment users by wellness intent (e.g., activity-focused vs recovery-focused)

---

## 🛠 Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## 📌 Key Takeaway

Wellness is multi-dimensional. While physical activity drives calorie expenditure, sleep supports recovery and weight reflects long-term behavior. Treating these metrics as complementary but independent pillars enables more accurate insights and more user-centered product design.

---

## 📎 Notes

- Sleep and weight data availability is lower than activity data and was handled intentionally during analysis.
- Correlation results describe relationships, not causation.

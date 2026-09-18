# Online Education Student Performance & Engagement Analysis

## 📌 Project Overview
This project analyzes student engagement, performance, and dropout patterns in an online learning environment. It combines SQL-based exploratory analysis with an interactive Power BI dashboard to help identify at-risk students, understand what drives performance, and surface actionable insights for improving retention.

## 📁 Project Files
| File | Description |
|---|---|
| `online_education_dataset.csv` | Raw dataset — 32,593 student records with 14 attributes covering demographics, engagement, and outcomes |
| `queries.sql` | SQL script with all exploratory analysis queries used to derive KPIs and insights |
| `sushma.pbix` | Power BI dashboard file visualizing the analysis interactively |

## 🗂️ Dataset Schema
| Column | Description |
|---|---|
| `id_student` | Unique student identifier |
| `gender` | Student gender (M/F) |
| `region` | Geographic region of the student |
| `highest_education` | Prior education level (e.g., HE Qualification, A Level, No Formal Quals) |
| `studied_credits` | Number of credits the student is enrolled for |
| `imd_band` | Index of Multiple Deprivation band (socioeconomic indicator, in %) |
| `total_clicks` | Total VLE (Virtual Learning Environment) clicks — proxy for engagement |
| `avg_score` | Student's average assessment score |
| `engagement_level` | Derived category: Low / Medium / High |
| `performance_level` | Derived category: Low / Medium / High |
| `risk_level` | Derived category: Safe / Low / High / Very High Risk |
| `pass_flag` | 1 if student passed, else 0 |
| `dropout_flag` | 1 if student withdrew, else 0 |
| `final_result` | Final outcome: Pass, Fail, Withdrawn, Distinction |

> Note: `imd_band`, `total_clicks`, `avg_score`, `engagement_level`, `performance_level`, and `risk_level` contain some missing values, likely due to incomplete activity records for certain students.

## 🎯 Objectives
- Measure overall student engagement (via clicks) and performance (via scores)
- Understand the relationship between engagement and academic outcomes
- Identify dropout drivers across engagement and performance segments
- Compare outcomes across regions and educational backgrounds
- Flag high-risk students for early intervention

## 🔍 Analysis Performed (`queries.sql`)
1. **Total Students** — overall count of unique learners
2. **Average Score & Average Clicks** — headline engagement/performance KPIs
3. **Pass & Dropout Summary** — total students who passed vs. dropped out
4. **Engagement Level Distribution** — student counts by Low/Medium/High engagement
5. **Performance Level Analysis** — student counts and average score by performance tier
6. **Risk Level Distribution** — student counts by risk category
7. **Engagement vs. Performance** — average score by engagement level
8. **Clicks vs. Score (Banded)** — average score across click-volume bands (0–500, 500–1000, 1000–2000, 2000–3000, 3000+)
9. **Dropout Rate by Engagement Level** — where dropout risk concentrates
10. **Dropout Rate by Performance Level** — link between low performance and withdrawal
11. **Regional Analysis** — students, average score, and average clicks by region
12. **Educational Background Analysis** — outcomes segmented by prior qualification level

## 📊 Dashboard (`sushma.pbix`)
The Power BI file visualizes the above SQL analysis, including:
- KPI cards for total students, average score, average clicks, pass/dropout counts
- Engagement, performance, and risk level breakdowns
- Engagement vs. performance and clicks vs. score trend visuals
- Regional and educational background comparisons
- Dropout rate analysis by engagement and performance segments

*Open with Power BI Desktop to explore interactively.*

## 🛠️ Tools Used
- **SQL** — data aggregation and KPI calculation
- **Power BI** — dashboarding and visualization
- **CSV** — source dataset

## 🚀 How to Use
1. Load `online_education_dataset.csv` into your SQL environment (e.g., MySQL, PostgreSQL, SQL Server).
2. Run `queries.sql` to reproduce all KPI tables.
3. Open `sushma.pbix` in Power BI Desktop to explore the visual dashboard (point it to the same dataset if prompted to refresh).

## 💡 Key Insight Themes
- Higher engagement (clicks) is generally associated with higher average scores.
- Dropout rates are concentrated among low-engagement and low-performance segments.
- Regional and prior-education differences correlate with variation in both engagement and outcomes.

---

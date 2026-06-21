🖥️ Developer Layoff Risk & Mental Health Dashboard

Power BI Dashboard Project

<img width="1458" height="802" alt="Image" src="https://github.com/user-attachments/assets/9b4a6bfd-b890-47d9-95ec-f873ce59f761" />

<img width="1380" height="802" alt="Image" src="https://github.com/user-attachments/assets/09561009-f2f6-49f0-ac87-06f9625555ec" />

<img width="1397" height="793" alt="Image" src="https://github.com/user-attachments/assets/e72b2aad-88b1-410a-9447-ad4069e98836" />

<img width="1393" height="811" alt="Image" src="https://github.com/user-attachments/assets/c33d8429-75b6-4425-a5ef-154c3ec7f9d1" />


📌 Project Overview

This Power BI dashboard analyzes the mental health, burnout, layoff risk, and productivity of 5,000 developers across India. The goal is to uncover patterns in how job roles, company types, work habits, and upskilling efforts relate to developer wellbeing and job security in an era of increasing layoffs and AI disruption.


📂 Dataset

DetailInfoFilelayoff_data.csvRows5,000 developersColumns50 featuresSourceDeveloper mental health & layoff risk survey data

Key Columns Used:


developer_id, gender, age, state, job_role
company_type, company_size, employment_type
stress_level, burnout_score, anxiety_score
sleep_hours, weekly_work_hours, work_life_balance_rating
high_layoff_risk, mentally_exhausted, likely_to_switch_job
job_security_confidence, ai_replacement_fear_score
upskilling_hours_per_week, salary_lpa, experience_years
github_activity_score, leetcode_problems_solved, certifications_count
primary_language, ai_tools_usage_hours_per_week



📊 Dashboard Pages


<img width="1458" height="802" alt="Image" src="https://github.com/user-attachments/assets/2bf9354a-93da-40dd-a9d5-f08d436fc5f9" />



Page 1 — Summary
High-level overview of the developer workforce

KPI Cards: Total Developers, High Layoff Risk Count, % Mentally Exhausted, % Likely to Switch
Gender Distribution — Donut chart
Company Type Breakdown — Donut chart
Total Developers by State — Bar chart
Job Role Distribution — Bar chart



Page 2 — Mental Health & Burnout



<img width="1380" height="802" alt="Image" src="https://github.com/user-attachments/assets/8d9b2f30-d7e5-449d-ad84-c4ccee454361" />



Deep dive into stress, burnout, and work-life balance
Burnout Risk Category (Low / Medium / High) — Donut chart
Average Stress Level by Job Role — Bar chart
Sleep Hours vs Work Hours — Scatter plot
Anxiety Score by Company Type — Bar chart
Work Life Balance Rating — Bar chart




Page 3 — Layoff Risk & Job Security



<img width="1397" height="793" alt="Image" src="https://github.com/user-attachments/assets/21d30d57-88a8-452f-bdb5-39b01e59d7ca" />






Who is at risk and how are they responding?

High Layoff Risk Count by Company Type — Bar chart
AI Replacement Fear Score — Bar chart
Job Security Confidence vs Experience Years — Scatter plot
Emergency Savings by Employment Type — Bar chart
LinkedIn Job Search Activity — Bar chart
Likely to Switch Job Breakdown — Donut chart



Page 4 — Skills & Productivity




<img width="1393" height="811" alt="Image" src="https://github.com/user-attachments/assets/d10ac390-6a7d-43fa-9dcf-63e6f5756c2f" />





How developers are upskilling amid uncertainty

Primary Language Distribution — Bar chart
AI Tools Usage Hours by Role — Bar chart
Upskilling Hours vs Salary — Scatter plot
GitHub Activity by Company Type — Bar chart
Certifications Count Distribution — Histogram
LeetCode Solved by Education Level — Bar chart



🧮 DAX Measures Created

daxTotal Developers = COUNTROWS(layoff_data)

High Layoff Risk Count =
COUNTROWS(FILTER(layoff_data, layoff_data[high_layoff_risk] = "Yes"))

% High Layoff Risk =
DIVIDE(
    COUNTROWS(FILTER(layoff_data, layoff_data[high_layoff_risk] = "Yes")),
    COUNTROWS(layoff_data)
) * 100

% Mentally Exhausted =
DIVIDE(
    COUNTROWS(FILTER(layoff_data, layoff_data[mentally_exhausted] = "Yes")),
    COUNTROWS(layoff_data)
) * 100

% Likely to Switch =
DIVIDE(
    COUNTROWS(FILTER(layoff_data, layoff_data[likely_to_switch_job] = "Yes")),
    COUNTROWS(layoff_data)
) * 100

Avg Burnout Score = AVERAGE(layoff_data[burnout_score])

Avg Stress Level = AVERAGE(layoff_data[stress_level])

Avg Anxiety Score = AVERAGE(layoff_data[anxiety_score])

Avg Job Security Confidence = AVERAGE(layoff_data[job_security_confidence])

Avg Upskilling Hours = AVERAGE(layoff_data[upskilling_hours_per_week])


💡 Key Insights


Service-based companies have the highest number of developers at high layoff risk
Developers working more hours per week sleep significantly fewer hours
ML Engineers and Cloud Engineers report the highest average stress levels
Developers with more experience tend to have higher job security confidence
Full Stack Developers form the largest job role group in the dataset
Maharashtra and Karnataka have the highest developer concentration



🛠️ Tools Used

ToolPurposePower BI DesktopDashboard building & visualizationPower QueryData cleaning & type transformationDAXCustom measures & KPI calculationsCSVRaw data source


📁 Repository Structure

📦 developer-layoff-dashboard
 ┣ 📊 layoff_data_analysis.pbix     # Power BI dashboard file
 ┣ 📄 layoff_data.csv               # Raw dataset
 ┗ 📝 README.md                     # Project documentation



👩‍💻 Author

Sofia Tabassum

Aspiring Data Analyst | Power BI | SQL | Python

📍Raigarh, Chhattisgarh , India

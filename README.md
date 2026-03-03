# [cite_start]Strategic Climate Data Narrative: Thailand's Path to 1.5°C [cite: 892, 893]

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)

📖 **[Read the Full Interactive Case Study on My Notion Portfolio](https://whispering-crater-183.notion.site/Project-Strategic-Climate-Data-Narrative-Thailand-s-Path-to-1-5-C-314e54702f0b80a0b72fda6af13ab862?source=copy_link)**

## 📌 Project Overview
This repository contains the Power BI data model and DAX code used to analyze Thailand's carbon emissions. The objective of this project was to develop a data-driven presentation advocating for systemic policy changes to keep global warming below the critical 1.5°C boundary. The final deliverable served as a persuasive tool for stakeholders to support the implementation of the proposed Thailand Climate Change Act.

This was a collaborative cohort project. My primary contributions focused on **Data Visualization (Power BI)** and **Policy Narrative Strategy**, specifically building the core analytical visuals (Slides 4–7).

## 🛠️ Tools & Technical Skills Highlighted
* **Tools:** Power BI, DAX
* **Data Source:** Our World in Data (OWID) CO2 dataset
* **Key Technical Implementations:**
  * **Context Management:** Utilized `CALCULATE`, `ALL`, and `ALLSELECTED` to dynamically manipulate filter contexts for global vs. local temperature comparisons.
  * **Advanced DAX Variables:** Structured complex formulas using `VAR` to isolate current vs. previous CO2 totals for clean, maintainable code.
  * **Dynamic Target Calculations:** Applied linear interpolation via DAX to establish exact future target budgets based on a 2019 baseline. 

## 💻 Technical Implementation: Advanced DAX
To ensure the dashboard dynamically calculated year-over-year variance and strict carbon budget targets, explicit DAX measures were engineered:

**Dynamic Waterfall Variance (CO2 Bridge):**
```dax
CO2 Bridge = 
VAR CurrentYear = SELECTEDVALUE('owid-co2-data'[year])
VAR FirstYear = MINX(ALLSELECTED('owid-co2-data'), 'owid-co2-data'[year])
VAR CurrentCO2 = SUM('owid-co2-data'[co2])
VAR PreviousCO2 = 
    CALCULATE(
        SUM('owid-co2-data'[co2]),
        FILTER(ALL('owid-co2-data'), 'owid-co2-data'[year] = CurrentYear - 1)
    )
RETURN 
IF(CurrentYear = FirstYear, CurrentCO2, CurrentCO2 - PreviousCO2)
```

**Interpolated Target Budget:**
```dax
Required_2023_Target1 = 
[GHG_2019_Baseline] - (([GHG_2019_Baseline] * 0.47) * ((2023 - 2019) / (2035 - 2019)))
```

## 📊 Executive Insights & Visual Proof (My Contributions)
**1. Rising Heat Signatures:** Proved Thailand's localized warming is outpacing global averages by engineering a comparative baseline metric.
<div align="center">
  <img width="767" height="437" alt="rising heat sig" src="https://github.com/user-attachments/assets/4d24cb97-2736-441d-9ca8-27f6235d6e3f" />
</div>

**2. Isolating the Primary Driver:** Identified CO2 as the overwhelming catalyst for the country's temperature increase through cumulative emission tracking.
<div align="center">
  <img width="751" height="456" alt="what is to blame" src="https://github.com/user-attachments/assets/1ffd5679-7f5c-403d-8194-4fde501af345" />
</div>

**3. The Expanding Footprint:** Demonstrated that carbon emissions are actively accelerating despite climate agreements by building a custom DAX Waterfall chart to calculate year-over-year CO2 variance.
<div align="center">
  <img width="693" height="373" alt="waterfall" src="https://github.com/user-attachments/assets/1796d334-d036-4d51-96f5-8014488e996d" />
</div>

**4. The Carbon Budget Deficit:** Visually proved Thailand has already exceeded its 2023 allowed GHG budget (Current: 416.85 | Target: 384.36) utilizing a dynamically filtered Gauge chart.
<div align="center">
  <img width="782" height="428" alt="gauge" src="https://github.com/user-attachments/assets/2a1bf599-42b8-47ff-89cf-eea3595f071f" />
</div>

## 📂 Repository Structure
* `/data` - Contains the raw OWID CO2 dataset used for the analysis.
* `/dashboard` - Contains the `Thailand_Climate_Project.pbix` Power BI file.
* [cite_start]`/presentation` - Contains the final collaborative slide deck PDF.

---
*If you are a recruiter or hiring manager, please visit the **[Notion Case Study](https://whispering-crater-183.notion.site/Project-Strategic-Climate-Data-Narrative-Thailand-s-Path-to-1-5-C-314e54702f0b80a0b72fda6af13ab862?source=copy_link)** to see how these technical deliverables were translated into actionable policy recommendations.*

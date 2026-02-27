# Strategic Climate Data Narrative: Thailand's Path to 1.5°C

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)

📖 **[Read the Full Interactive Case Study on My Notion Portfolio]([https://whispering-crater-183.notion.site/Project-Strategic-Climate-Data-Narrative-Thailand-s-Path-to-1-5-C-314e54702f0b80a0b72fda6af13ab862?source=copy_link])**

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

## 📊 Key Analytical Visuals (My Contributions)
1. **Rising Heat Signatures:** Comparative line charting tracking Thailand's annual greenhouse gas temperature change relative to the global baseline.
2. **Isolating the Primary Driver:** Analysis identifying CO2 as the primary driver of the country's temperature increase.
3. **The Expanding Footprint:** A custom Waterfall chart calculating incremental year-over-year CO2 variance to dramatically highlight emission trends despite climate agreements.
4. **The Carbon Budget Deficit:** A Gauge chart proving Thailand exceeded its 2023 allowed GHG budget (Current: 416.85 | Target: 384.36).

## 📂 Repository Structure
* `/data` - Contains the raw OWID CO2 dataset used for the analysis.
* `/dashboard` - Contains the `Thailand_Climate_Project.pbix` Power BI file.
* `/presentation` - Contains the final collaborative slide deck PDF.

---
*If you are a recruiter or hiring manager, please visit the **[Notion Case Study]([Insert_Your_Notion_Link_Here])** to see how these technical deliverables were translated into actionable policy recommendations.*

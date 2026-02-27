# Strategic Climate Data Narrative: Thailand's Path to 1.5°C

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)

📖 **[Read the Full Interactive Case Study on My Notion Portfolio]([https://whispering-crater-183.notion.site/Project-Strategic-Climate-Data-Narrative-Thailand-s-Path-to-1-5-C-314e54702f0b80a0b72fda6af13ab862?source=copy_link])**

## 📌 Project Overview
[cite_start]This repository contains the Power BI data model and DAX code used to analyze Thailand's carbon emissions[cite: 565]. [cite_start]The objective of this project was to develop a data-driven presentation advocating for systemic policy changes to keep global warming below the critical 1.5°C boundary[cite: 565, 566]. [cite_start]The final deliverable served as a persuasive tool for stakeholders to support the implementation of the proposed Thailand Climate Change Act[cite: 567].

This was a collaborative cohort project. [cite_start]My primary contributions focused on **Data Visualization (Power BI)** and **Policy Narrative Strategy**, specifically building the core analytical visuals (Slides 4–7)[cite: 564, 575].

## 🛠️ Tools & Technical Skills Highlighted
* [cite_start]**Tools:** Power BI, DAX [cite: 564]
* **Data Source:** Our World in Data (OWID) CO2 dataset
* **Key Technical Implementations:**
  * [cite_start]**Context Management:** Utilized `CALCULATE`, `ALL`, and `ALLSELECTED` to dynamically manipulate filter contexts for global vs. local temperature comparisons[cite: 582, 583, 619].
  * [cite_start]**Advanced DAX Variables:** Structured complex formulas using `VAR` to isolate current vs. previous CO2 totals for clean, maintainable code[cite: 618].
  * [cite_start]**Dynamic Target Calculations:** Applied linear interpolation via DAX to establish exact future target budgets based on a 2019 baseline [cite: 653, 665-668]. 

## 📊 Key Analytical Visuals (My Contributions)
1. [cite_start]**Rising Heat Signatures:** Comparative line charting tracking Thailand's annual greenhouse gas temperature change relative to the global baseline[cite: 577, 578].
2. [cite_start]**Isolating the Primary Driver:** Analysis identifying CO2 as the primary driver of the country's temperature increase[cite: 602, 603].
3. [cite_start]**The Expanding Footprint:** A custom Waterfall chart calculating incremental year-over-year CO2 variance to dramatically highlight emission trends despite climate agreements[cite: 611, 614, 615].
4. [cite_start]**The Carbon Budget Deficit:** A Gauge chart proving Thailand exceeded its 2023 allowed GHG budget (Current: 416.85 | Target: 384.36)[cite: 647, 650, 651].

## 📂 Repository Structure
* `/data` - Contains the raw OWID CO2 dataset used for the analysis.
* `/dashboard` - Contains the `Thailand_Climate_Project.pbix` Power BI file.
* `/presentation` - Contains the final collaborative slide deck PDF.

---
*If you are a recruiter or hiring manager, please visit the **[Notion Case Study]([Insert_Your_Notion_Link_Here])** to see how these technical deliverables were translated into actionable policy recommendations.*

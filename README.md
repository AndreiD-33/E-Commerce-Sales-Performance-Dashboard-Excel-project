# E-Commerce Sales Performance Dashboard

![Dashboard Demo](https://github.com/user-attachments/assets/89e81a22-3e48-4161-a854-73954eb93bb1)


## Introduction

As a data analyst passionate about transforming raw data into strategic decision-making tools, I noticed a gap in many standard portfolios: dashboards often look cluttered or fail to answer core business questions while ignoring the underlying data architecture. I set out to build a professional, executive-level **E-Commerce Sales Performance Dashboard** entirely in Excel, proving that advanced Excel can rival dedicated BI solutions when using proper relational modeling.

The goal of this project is to track financial performance (*Net Income*), analyze revenue concentration (*Pareto principle*), evaluate customer value, and monitor logistical risks through a clean, interactive user interface supported by a robust data pipeline.

## Questions to Analyze

To uncover actionable insights from the e-commerce dataset, I structured the analysis around the following core questions:
* What are the primary revenue drivers according to the **80/20 Pareto principle**?
* How does net income fluctuate across quarters and years (*seasonality*)?
* What is the geographic distribution of sales across regions and counties?
* Which customer segments and products drive higher **Average Revenue Per User (ARPU)**?
* Which product subcategories exhibit the highest return rates for logistics optimization?

## Excel Skills & Technologies Used

The following advanced Excel and Business Intelligence skills were utilized for this end-to-end project:
* 🔄 **Power Query (ETL):** Data extraction, transformation, cleaning, and table consolidation.
* 💪 **Power Pivot & Data Modeling:** Relational database architecture (*Star Schema*).
* 🧮 **DAX (Data Analysis Expressions):** Custom financial and operational measures.
* 📊 **Advanced Pivot Tables & Charts:** Combo charts, geographical maps, dynamic Top-N filtering.
* 🎨 **UI/UX Design Principles:** Executive layouts, secondary axes, and custom number formatting (*K/M RON*).

## Data Architecture & ETL Process

A major focus of this project was building a reliable data pipeline, transitioning from a highly fragmented raw database to an optimized analytical model.

### 📥 Extract & Transform (Power Query)
I started with a highly normalized raw database containing fragmented tables (e.g., separate tables for regions, counties, cities, and user demographics). 
Using **Power Query**, I merged, cleaned, and shaped the data. For instance, in the `Dim_Clienti` (*Customers*) table, I applied transformation steps to resolve nulls and errors, achieving **100% valid data quality** for demographic analysis.

![Power Query ETL](https://github.com/user-attachments/assets/aefbcc36-c57a-4851-89d3-66d2f6f51540)

### 🏗️ Data Modeling (Star Schema)
To ensure maximum performance for DAX calculations, I transformed the raw relational model into a clean **Star Schema** using **Power Pivot**. 
The model is logically organized into:
* **Dimension Tables (`Dim`)**: `Dim_Promotii`, `Dim_Produse`, `Dim_Timp`, `Dim_Clienti`.
* **Fact Tables (`Fact`)**: `Fact_Retururi`, `Fact_Comenzi`, `Fact_Facturi`.

![Star Schema Data Model](https://github.com/user-attachments/assets/c13428b4-6ab7-40ca-8c38-b22b53264151)

---

## 1️⃣ Financial Performance & Time Intelligence

🧮 **Skills:** *Power Pivot*, *DAX*, *Pivot Charts*

**Analysis:**
* Built a dedicated date table (`Dim_Timp`) to enable advanced time intelligence.
* Created an evolutionary net income trend analysis segmented by quarters and years.
* Applied custom number formatting (`1,6M RON`, `500K RON`) directly to the chart axes to improve readability for executive stakeholders.

**💡 Insights:**
* Clear seasonal spikes appear across specific quarters, indicating predictable demand cycles that can inform inventory planning.

## 2️⃣ Revenue Concentration (Pareto Analysis)

📊 **Skills:** *Advanced DAX*, *Combo Charts*, *Secondary Axis*

**Analysis:**
* Developed a DAX measure combining `CALCULATE`, `ALL`, and `FILTER` to compute running cumulative percentages for subcategories.
* Built a combo chart pairing **Net Income** columns (*Primary Axis*) with **Cumulative Percentage** lines (*Secondary Axis*, strictly locked at 100% maximum).

**💡 Insights:**
* **80/20 Rule Validation:** The top 6 subcategories (such as *Ankle Boots*, *Over Knee Boots*, and *Knee High Boots*) generate nearly **78% of total net income**.
* **Strategic Impact:** Directs marketing focus and supply chain priorities toward high-margin, high-volume product lines.

## 3️⃣ Geographic & Demographic Distribution

🗺 **Skills:** *Map Visuals*, *Slicer Connections*, *UI/UX*

**Analysis:**
* Connected regional and county data to dynamic map visualizations using intermediate lookup structures.
* Implemented an isolated Donut Chart for gender distribution that reacts to global time/location filters while remaining independent of direct gender overrides, preserving comparative context.

**💡 Insights:**
* Sales show a high concentration in major urban hubs (e.g., *Bucharest-Ilfov*, *Central region*).
* The gender contribution is highly balanced across historical purchases, requiring broad demographic marketing strategies.

## 4️⃣ Executive KPIs & Logistical Risk Analysis

⚙️ **Skills:** *Custom DAX Measures* (`DISTINCTCOUNT`, `DIVIDE`), *Top-N Filtering*, `GETPIVOTDATA`

**Analysis:**
* Calculated high-level strategic KPIs: **Number of Unique Customers**, **Return Rate**, **Products Sold**, **Net Income**, and **Average Revenue Per User (ARPU)**.
* Configured a dynamic Top-3 subcategory matrix based on return rates, directly linked to a Pivot Table to highlight logistical issues on the fly.

**💡 Insights:**
* **ARPU Tracking:** Provides immediate visibility into customer spending efficiency (**1.397,85 RON** average per user).
* **Logistics Optimization:** Pinpointed specific subcategories (e.g., *Summer Scarves*, *Skinny Belts*) with disproportionately high return rates (reaching over **36%**), providing an actionable target for the quality assurance and supply chain teams.

---

## Conclusion

This project demonstrates how advanced Excel features can support an end-to-end data pipeline. By taking raw transactional logs, applying rigorous ETL processes via **Power Query**, structuring a **Star Schema** in **Power Pivot**, and writing advanced **DAX** formulas, I was able to build an interactive executive dashboard. Featuring Pareto analysis, geographic mapping, and logistical risk tracking, this repository serves as a complete blueprint for data-driven decision-making in the e-commerce sector.





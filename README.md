## Production Data Analysis - PU Wing & Body Refrigerator Assembly Lines

### 🗂️ Project Overview
This project analyzes real-world production data collected from multiple assembly teams
at a manufacturing facility, including the PU Wing, PU Body, TLR, SPU, and HT lines.
Data is recorded per shift (day/night), capturing output by product code, workforce size,
operating hours, and the key efficiency metric UPPH (Units Per Person Per Hour).

### 📷 Screenshot
![Slicer Dashboard](Screenshot/SlicerDashboard.png)
![Combo Chart](Screenshot/ComboChart.png)
### 📁 Data Description
* Data is recorded per shift (day/night), capturing output by product code, workforce size,
operating hours, and the key efficiency metric UPPH (Units Per Person Per Hour).
* Output volume by product code (51CD, 71, 91, 1.6, 3.2, 10.6, ...)
* Headcount per shift
* Shift start/end times, lunch break, dinner break, short breaks, and 5S time
* Actual UPPH vs. Demand targets
* Incident notes: line breakdowns, material shortages, mold issues, etc.
### ⚙️ Data Pipeline – Power Query (ETL)
* Raw data from daily shift reports was consolidated and cleaned using Power Query
before being loaded into the analysis layer.
* Extract: Imported raw shift records from multiple source sheets
* Transform: Standardized date/time formats, handled missing values, split day/night shifts, renamed and reordered columns for consistency
* Load: Output a single clean, structured table ready for Pivot analysis
### 📊 Dashboard & Visualization
An interactive Excel dashboard was built on top of the cleaned data,
designed for non-technical production managers to explore performance at a glance.
**Interactive Filters (Slicers)**
- 📅 **Month** – Compare performance across time periods
- 🏭 **Assembly Line** – Drill into PU Wing, PU Body, TLR, SPU, or HT
- 👥 **Team** – Isolate individual team performance within a line
**Charts & Tables**
- 📈 **UPPH Trend Chart** (Pivot Chart) – Actual vs. Demand by day/week
- 📦 **Output Summary Table** (Pivot Table) – Total units by product code,
  broken down by line and team
- 👷 **Workforce Utilization Table** – Headcount vs. output ratio per shift
**Design Principles**
- All visuals update dynamically when slicers are changed
- Color-coded conditional formatting highlights underperforming shifts
  (UPPH below demand threshold)
- Layout optimized for a single-screen view — no scrolling required
### 🛠️ Tool used
* Microsoft Excel (power query, combo chart, formulas, pivot tables, conditional formatting, advand formulas) 
  * Power query: Data extraction, cleaning, and transformation (ETL)
  * Pivot Table: Multi-dimensional data summarization
  * Pivot Chart + Slicer: Interactive visual dashboard with dynamic filtering
  * Conditional Formatting: Visual alerts for KPI thresholds
  * Excel Formulas: Working hour calculations, UPPH computation

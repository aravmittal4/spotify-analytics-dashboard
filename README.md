# 🎵 Spotify Listening Insights – Power BI Dashboard

## 📌 Overview
This project presents an interactive **Power BI dashboard** built to analyze Spotify listening patterns and uncover insights into user engagement, music preferences, and behavioral trends.  
The solution demonstrates advanced **Power BI capabilities** including **Power Query Editor transformations**, **custom DAX measures**, **calculated columns**, **data modeling**, and the **drill-through feature** to provide both high-level summaries and deep-dive explorations.

By integrating robust analytics with clear visual storytelling, the dashboard turns raw listening history into actionable insights.

---

## 🎯 Objectives
- Track the total number of albums, artists, and tracks played over time.
- Compare listening patterns between **weekdays and weekends**.
- Conduct **Latest Year vs Previous Year (LY vs PY)** comparisons with **YoY growth analysis**.
- Identify **Top 5 albums, artists, and tracks** dynamically.
- Discover peak listening hours using a heat map visualization.
- Categorize tracks via **Quadrant Analysis** (listening time vs play frequency).
- Provide a **drill-through-enabled details grid** for granular exploration with CSV export.

---

## 🛠 Data Preparation & Transformation
**Using Power Query Editor:**
- Created a **Calendar Table** for time intelligence functions.
- Extracted **date** and **time** from the timestamp (`ts`) column.
- Changed data types to ensure consistent date/time formatting.
- Added calculated columns for:
  - `Track Played Date`
  - `Track Played Time`
  - `Day Name`
  - `Weekday/Weekend` flag
  - `Hour`
  - `Day Number by Week`

---

## 🧮 DAX Measures
Over **20 custom measures** were created to power the dashboard:
- **Distinct Counts**: Number of unique albums, artists, and tracks.
- **Min/Max Year** detection for trend analysis.
- **LY, PY, and YoY Growth KPIs** for albums, artists, and tracks.
- **Quadrant Analysis Metrics**:
  - Average Listening Time (mins)
  - Track Frequency
  - Conditional Formatting measure for quadrant visuals.
- **Dynamic Parameters** for listening time and frequency to control visual segmentation.

---

## 🗂 Data Modeling
The data model for this project is designed for simplicity and performance, connecting key tables to enable time-based and measure-driven analysis.

**Tables Used:**
- **spotify_history** *(Fact Table)*: Contains core listening history data such as platform, start/stop reasons, shuffle/skipped flags, track details, and calculated columns for track played date/time.
- **Date table** *(Dimension Table)*: Custom calendar table created in Power Query with fields for Date, Day Name, Day Number in Week, Weekday/Weekend flag, and Year.
- **listening time (mins)** *(Measure/Calculation Table)*: Contains calculated measures for average listening time in minutes and related KPIs.

**Relationships:**
- `spotify_history[Track played date]` → `Date table[Date]` (Many-to-One, Single Direction)
- Measure table (`listening time (mins)`) is independent and used to store DAX measures for easier maintenance.

**Why this structure?**
- The **fact table** (`spotify_history`) stores detailed event-level records.
- The **date dimension** enables powerful time intelligence calculations for YoY, LY vs PY, and trend analysis.
- The **measure table** keeps all KPIs and calculations organized, reducing complexity in the main tables.

---

## 🔍 Dashboard Features
- **Drill-Through Pages**: Click on any album, artist, or track to open a detailed view with metrics and visual breakdowns.
- **Interactive Charts**: Time series, scatter plots, KPI cards, pie charts, and heat maps.
- **Top 5 Leaderboards**: Auto-updating rankings for albums, artists, and tracks.
- **Weekday vs Weekend Analysis**: Quickly toggle between day types.
- **Quadrant Scatter Plot**: Classifies tracks into high/low frequency & listening time categories.
- **Exportable Detail Grid**: View raw-level data and export directly to CSV.

---

## 💡 Key Insights
1. Listening peaks between **8 PM – 11 PM**, especially on weekends.
2. Certain niche tracks show **low frequency but high listening time**, indicating loyal audiences.
3. Year-over-year growth in unique artists suggests expanding listener variety.

---

## 📂 Repository Structure

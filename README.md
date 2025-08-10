# 🎵 Spotify Listening Insights – Power BI Dashboard

## 📌 Overview
This project analyzes Spotify listening patterns to uncover trends in user engagement, music preferences, and peak listening periods.  
Built using **Power Query Editor**, **DAX calculations**, and optimized **data modeling**, the interactive Power BI dashboard enables deep dives into albums, artists, and tracks over multiple years.

The goal is to demonstrate how data analytics and visualization can transform raw streaming data into **actionable insights**.

---

## 🎯 Objectives
- Track total albums, artists, and tracks played over time.
- Compare listening patterns between **weekdays and weekends**.
- Analyze **Latest Year vs Previous Year (LY vs PY)** trends and **YoY growth**.
- Identify **Top 5 albums, artists, and tracks** dynamically.
- Discover peak listening hours using heat map analysis.
- Classify tracks using **Quadrant Analysis** (listening time vs frequency).
- Provide an interactive details grid with **drill-through** and **CSV export**.

---

## 🛠 Data Preparation & Modeling
- **Power Query Editor**:
  - Created Calendar Table for time intelligence.
  - Extracted date & time from timestamp.
  - Added calculated columns: day name, weekday/weekend flag, hour, day number by week.
- **Data Modeling**:
  - Implemented a **star schema** linking fact and dimension tables.
  - Ensured optimized relationships for performance.
- **DAX Measures**:
  - 20+ custom calculations for KPIs, LY/PY comparisons, YoY growth %, quadrant classification, and conditional formatting.

---

## 📊 Key Features
- Interactive charts with slicers and filters.
- Drill-through pages for granular insights.
- Weekday vs weekend trend comparison.
- Heat map of listening activity by hour/day.
- Quadrant scatter plot for engagement analysis.
- Top 5 leaderboards for albums, artists, and tracks.

---

## 💡 Key Insights
1. Listening peaks between **8 PM – 11 PM**, especially on weekends.
2. Certain niche tracks have **low frequency but high listening time**, indicating loyal audience segments.
3. Year-over-year growth in unique artists played, showing diversification in music preferences.

---


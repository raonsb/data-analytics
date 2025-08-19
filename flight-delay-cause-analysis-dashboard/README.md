# Flight Delay Cause Analysis

*A Data Analytics Portfolio Project by Raon Spielberg Berek*

➡️ [View the Interactive Dashboard on Tableau Public](https://public.tableau.com/views/USFlightDelayCauseAnalysisDashboard/USFlightDelayAnalysis?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
➡️ [View the Full Presentation](presentation/)

---

## 1. Business Understanding

### Background

The aviation industry relies heavily on time efficiency to maintain smooth operations. Flight delays represent a recurring issue that leads to significant financial losses for airlines. Delays negatively impact customer satisfaction and trust. They also disrupt airport efficiency and overall operational performance.

### Dataset Provided

* **Name:** Airline On-Time Statistics and Delay Causes
* **Source:** Bureau of Transportation Statistics (BTS), USA
* **Time Range:** May 2023 – May 2025
* **Coverage:** Flight schedules, delays, and their contributing factors

### Problem Statements

Based on the background, management needs, and the dataset provided, the following problem statements are addressed:

1. What are the different types of flight delays and how many delays fall into each category?
2. What are the top-ranking causes of flight delays based on their frequency of occurrence?
3. How do carrier-related delays rank in terms of total delay counts?
4. How has the average percentage of carrier-related delays changed over time?
5. How is the total delay distributed across U.S. states and cities?

### Project Objectives

To address the identified problem statements, the following project objectives are defined. An interactive dashboard was developed with filters for **month, year, airport name, state, and city**, featuring:

1. **Scorecards** displaying the total number of delays and the count of each delay type.
2. **Bar chart** showing the ranking of delay causes by frequency of occurrence.
3. **Bar chart** ranking airlines based on the number of carrier-related delays.
4. **Line chart** illustrating the trend of the average carrier delay percentage over time.
5. **Map chart** highlighting flight delay hotspots across U.S. states and cities.

---

## 2. Data Understanding

* **Columns:** 21 (flight statistics and delay causes)
* **Delay Indicator (arr\_del15):**  ≥15 minutes → Delay, <15 minutes → On-Time
* **Records:** 47,097 rows (May 2023 – May 2025)
* **Missing Values:** 57 rows
* **Data Types:** 4 text, 12 whole number, 5 decimal

---

## 3. Data Preparation

* Dropped 9 irrelevant columns: `arr_flights`, `arr_cancelled`, `arr_diverted`, and delay duration columns (`arr_delay`, `carrier_delay`, `weather_delay`, `nas_delay`, `security_delay`, `late_aircraft_delay`).
* Removed 57 rows with missing values.
* Created new **date** column (Month-Year format).
* Extracted **city** and **state** from `airport_name` into separate columns, and trimmed extra spaces.

---

## 4. Modeling & Evaluation (Tableau Worksheets and Dashboard)

### Viz 1 – Delay Categories

* Displays total count of delays for five categories: Carrier, Late Aircraft, NAS, Security, and Weather.
* **Insight:** Late Aircraft Delay dominates (>1.1M incidents), Security Delay is minimal (<8.5K incidents).

### Viz 2 – Top Causes of Delay

* **Top 3:** Late Aircraft, Carrier, and NAS Delays.
* **Insight:** Internal operational issues (Late Aircraft & Carrier) drive most delays. Weather and Security have minimal impact. Improvement focus: turnaround efficiency & crew scheduling.

### Viz 3 – Carrier-Specific Delays

* A small group of airlines (Southwest, American, SkyWest) lead in self-inflicted delays.
* **Insight:** Top 5 airlines account for a disproportionate share of carrier delays. Efforts should prioritize these airlines.

### Viz 4 – Seasonal Trend

* Carrier-caused delay percentage follows a predictable cycle: best in **winter (Jan)**, worst in **late summer–fall (Aug–Nov)**, peaking in **October**. Secondary peak in spring.
* **Insight:** Delay percentage fluctuates \~10 points annually (34%–45%). Airlines must use seasonality for proactive planning.

### Viz 5 – Geographic Hotspots

* Delays concentrated in major hubs: **NYC, Chicago, Atlanta, California, Denver, Dallas**.
* **Insight:** Focus on top 15 hotspot airports for maximum national impact.

### Dashboard Summary

* Delays are massive but concentrated in **key hubs & major airlines**.
* Majority caused by **internal operations** (Late Aircraft & Carrier).
* Delays follow **predictable seasonal cycles**.
* Strategy: **Target hotspot hubs + plan for seasonal peaks**.

---

## 5. Key Conclusions

1. **The Problem is Concentrated** – Delays heavily cluster in key hubs and airlines.
2. **The Root Cause is Operational** – Internal inefficiency drives most delays, not external factors.
3. **The Pattern is Predictable** – Seasonal cycles allow proactive measures.

---

## 6. Strategic Recommendations

| Recommendation                                          | Why                                                        | Proposed Action                                                                                                       |
| ------------------------------------------------------- | ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **1. Launch a Targeted Efficiency Program at Key Hubs** | Delays are operational and concentrated in a few airports. | Conduct deep-dive reviews of turnaround processes & crew scheduling at the top 15 hotspot airports.                   |
| **2. Implement Proactive, Seasonal Resource Planning**  | Performance peaks negatively in late Summer & Fall.        | Develop enhanced resource allocation plans for ground staff, technicians, and reserve crews before high-risk periods. |

---

## 7. Repository Structure

```
/data          # Raw dataset file used for the analysis
/presentation  # Final PowerPoint presentation (.pptx and .pdf)
README.md      # Project documentation
```

---

## 8. Contact

**Name:** Raon Spielberg Berek

**Email:** raonbereknew@gmail.com

**LinkedIn:** [linkedin.com/in/raonspielbergberek](https://www.linkedin.com/in/raonspielbergberek)

**Instagram:** [@raonsb](https://www.instagram.com/raonsb)



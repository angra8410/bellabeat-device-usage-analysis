# Analysis Summary

This document summarizes the key findings from the Bellabeat smart device usage analysis, derived from SQL stored procedures applied to non-Bellabeat sma device data. The goal is to extract actionable insights on user behavior and device interaction patterns.

---

## 1. Seasonality Patterns

**Weekly Trends:**  
- Device usage exhibits clear weekly seasonality.
- **Peak activity** is observed on **Wednesdays (Avg: 5.37)**, **Mondays (5.05)**, **Saturdays (5.02)**, and **Fridays (4.85)**.
- **Lowest activity** is seen on **Tuesdays (3.49)** and **Sundays (4.32)**.
- This suggests mid-week and weekend periods are particularly important for user engagement.

**Monthly Trends:**  
- Usage increases substantially from **March (3.48)** to **April (4.89)**, indicating possible seasonal drivers or the effect of New Year’s resolutions wearing off and springtime activity increasing.

---

## 2. Usage Trends

- **Heavy Users Identified:**  
  The data shows a wide range of average usage values, with the most active users recording values above **3,400**, and the least active below **1,400**.
- **Active vs. Inactive Cohorts:**  
  The segmentation output shows a split between "Active" and "Inactive" users, with active users consistently maintaining higher average usage.
- **Trend Implication:**  
  This implies the presence of a core group of highly engaged users, but also highlights a significant portion of less engaged (or churn-risk) users.

---

## 3. Active Time of Day

- **Afternoon and Night Lead in Activity:**  
  - **Afternoon:** Highest step counts (**162,481 steps**) and substantial calories burned.
  - **Night:** Also high activity (**152,416 steps**), with the highest calorie counts (**23,905**).
  - **Morning:** Less activity (**92,601 steps**), but still meaningful engagement.
- **Sleep Patterns:**  
  - Sleep duration varies, ranging from **~5h 16m to 9h 49m** per night, with some days showing significant drops (e.g., 1h 1m), possibly due to data gaps or outlier days.

---

## 4. User Segmentation

- **Two Distinct Segments:**  
  - **Active Users:** Maintain high average trend values (above ~2,000), representing the most engaged group.
  - **Inactive Users:** Lower average values (mostly below ~2,000), potentially at higher risk for churn or disengagement.
- **Engagement Opportunity:**  
  Marketing and product features can be tailored for each segment—for example, re-engagement campaigns for inactive users or advanced feature promotion for actives.

---

## Key Takeaways

- **Engagement peaks midweek and on weekends**, suggesting campaign timing should leverage these windows.
- **Springtime sees a rise in activity**, indicating seasonal promotions or challenges could be effective.
- **Afternoons and nights are prime times for user activity**, which can guide notification timing and feature rollouts.
- **A substantial inactive segment exists**, representing an opportunity for targeted re-engagement or lifecycle marketing.

---

These insights provide a data-driven foundation for Bellabeat’s marketing and product strategies, enabling more precise targeting, personalized user experiences, and improved user retention.

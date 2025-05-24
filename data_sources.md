# Data Sources Description

This analysis is based on data extracted from four key stored procedures in the Bellabeat analytics database. Each stored procedure provides a unique perspective on smart device usage patterns among users of non-Bellabeat devices.

---

## 1. `sp_Bellabeat_SeasonalityPatterns`

**Purpose:**  
Analyzes average device usage trends by day of the week and by month, identifying weekly and monthly seasonality in user activity.

**Sample Output:**  
**By Day of Week:**
| DayOfWeek  | AvgTrendValue |
|------------|---------------|
| Sunday     | 4.32          |
| Monday     | 5.05          |
| Tuesday    | 3.49          |
| Wednesday  | 5.37          |
| Thursday   | 4.85          |
| Friday     | 4.85          |
| Saturday   | 5.02          |

**By Month:**
| Month | AvgTrendValue |
|-------|--------------|
| March | 3.48         |
| April | 4.89         |

---

## 2. `sp_Bellabeat_Usage_Trends`

**Purpose:**  
Returns average usage values for individual users/devices, allowing for trend analysis and identification of heavy/light users.

**Sample Output:**
| Id         | AvgTrendValue |
|------------|--------------|
| 8877689391 | 3451.17      |
| 8378563200 | 3356.17      |
| ...        | ...          |
| 1624580081 | 1352.89      |

---

## 3. `sp_Bellabeat_UserActiveTimeOfDay`

**Purpose:**  
Examines user activity by time of day (morning, afternoon, night) and over specific dates, including steps taken, calories burned, and sleep duration.

**Sample Output:**

**By Time of Day:**
| TimeOfDay  | Steps | Calories |
|------------|-------|----------|
| Morning    | 92601 | 15980    |
| Afternoon  |162481 | 20439    |
| Night      |152416 | 23905    |

**Daily Activity and Sleep Example:**
| Date       | Steps | Sleep Duration |
|------------|-------|---------------|
| 2016-03-13 | 441   | 7h 21m        |
| 2016-03-14 | 423   | 7h 3m         |
| ...        | ...   | ...           |
| 2016-04-11 | 351   | 5h 51m        |

---

## 4. `sp_Bellabeat_UserSegmentation`

**Purpose:**  
Segments users by their average usage into categories such as "Active" and "Inactive" for cohort analysis and targeted insights.

**Sample Output:**
| Id         | AvgTrendValue | UserSegment |
|------------|---------------|-------------|
| 8877689391 | 3451.17       | Active      |
| 8378563200 | 3356.17       | Active      |
| ...        | ...           | ...         |
| 1624580081 | 1352.89       | Inactive    |

---

## Data Source Notes

- All data was generated via direct calls to these stored procedures in the company SQL database.
- Data covers activity, usage, and engagement metrics, enabling both quantitative analysis and behavioral segmentation.
- For privacy, user/device IDs are anonymized.

---

This documentation ensures all data sources and their outputs are transparent for reproducibility and further analysis.

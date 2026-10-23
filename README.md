# Bike Buyers Analysis Dashboard (Excel Project)

An end-to-end Excel data analysis project that cleans a raw customer dataset, summarizes it with PivotTables, and presents the results in an interactive dashboard to understand **who buys bikes**.


## Project Overview

A bike retailer wants to know which customers are most likely to buy a bike. Using a dataset of 1,000 customers, this project explores how **gender, income, commute distance and age** relate to bike purchases, and wraps the findings in a dashboard with slicers so the data can be filtered by **marital status, education and region**.

**Business question:** Which customer segments are most likely to purchase a bike?

## 🗂 Repository Structure

```
├── raw excel/
│   └── Raw_Bike_Buyers_Data.xlsx
├── Processed Excel/
│   └── Bike_Buyers_Dashboard.xlsx
├── images/
│   └── Bike_Buyers_Excel_Dashboard_ScreenShot.png
└── README.md
```

The dashboard workbook has four sheets:

1. **bike_buyers** – a copy of the raw data
2. **Working Sheet** – the cleaned data plus the new *Age Bracket* column
3. **Pivot Table** – the PivotTables and charts that feed the dashboard
4. **Dashboard** – the final, interactive report

## Dataset

Each row is one customer.

| Column | Description |
|--------|-------------|
| ID | Unique customer ID |
| Marital Status | Married / Single |
| Gender | Male / Female |
| Income | Annual income |
| Children | Number of children (0–5) |
| Education | High School, Partial College, Bachelors, Graduate Degree, etc. |
| Occupation | Professional, Clerical, Management, Manual, Skilled Manual |
| Home Owner | Yes / No |
| Cars | Number of cars owned (0–4) |
| Commute Distance | 0-1, 1-2, 2-5, 5-10, 10+ miles |
| Region | North America, Europe, Pacific |
| Age | Customer age |
| Purchased Bike | **Target variable** — Yes / No |

## Data Cleaning & Preparation

- **Removed 26 duplicate records** (1,026 → 1,000 unique customers).
- **Standardized abbreviations** into readable labels: `M`/`S` → Married/Single and `M`/`F` → Male/Female.
- **Standardized commute labels** (`10+ Miles` → `More Than 10 Miles`) so categories sort and read consistently.
- **Created an `Age Bracket` column** with an Excel formula:
  - Adolescent 0–30
  - Middle Age 31–54
  - Old 55+
- Checked for missing values: none were found.

## Tools & Techniques

- **Microsoft Excel**
- Data cleaning (remove duplicates, find & replace)
- Formulas (nested `IF` for age brackets)
- PivotTables and PivotCharts
- Slicers for interactive filtering
- Dashboard design

## Key Findings

Overall, **481 of 1,000 customers (48.1%) purchased a bike.**

### 1. Age is the strongest driver of purchases
| Age Bracket | Customers | Bought a bike | Purchase rate |
|-------------|----------:|--------------:|--------------:|
| Middle Age (31–54) | 719 | 388 | **54.0%** |
| Adolescent (0–30) | 110 | 39 | 35.5% |
| Old (55+) | 171 | 54 | 31.6% |

Middle-aged customers make up **72% of the customer base** and account for **~81% of all bike purchases**. Purchases peak between roughly ages 34–38.

### 2. Shorter commutes mean more purchases
| Commute Distance | Customers | Bought a bike | Purchase rate |
|------------------|----------:|--------------:|--------------:|
| 0–1 miles | 366 | 200 | 54.6% |
| 1–2 miles | 169 | 77 | 45.6% |
| 2–5 miles | 162 | 95 | **58.6%** |
| 5–10 miles | 192 | 76 | 39.6% |
| More than 10 miles | 111 | 33 | **29.7%** |

Customers commuting **under 5 miles** are the most likely buyers, while those commuting **10+ miles** are the least likely. Purchase rates fall noticeably past the 5-mile mark.

### 3. Buyers earn more on average, and men earn more than women
| Gender | Avg income (non-buyers) | Avg income (buyers) |
|--------|------------------------:|--------------------:|
| Female | $53,440 | $55,774 |
| Male | $56,208 | $60,124 |
| **All** | $54,875 | **$57,963** |

Buyers have a higher average income than non-buyers in both genders, and the income gap between men and women exists in both groups. Purchase rates by gender are almost identical (female 48.9% vs. male 47.4%), so **gender alone is not a useful targeting factor**.

### 4. Additional insights from the cleaned data
*These come from supplementary analysis of the `Working Sheet`, not from the dashboard charts.*

- **Region:** Pacific has the highest purchase rate (58.9%), followed by Europe (49.3%) and North America (43.3%).
- **Marital status:** Single customers buy more often (54.1%) than married customers (42.9%).
- **Education:** Customers with a Bachelors (55.2%) or Graduate degree (54.0%) buy more than those with partial high school (26.3%).
- **Cars:** Customers with 0–1 cars buy at 57–61%, versus 36–39% for those with 2 or more cars.

## Recommendations

1. **Target 31–54-year-olds**, the largest and highest-converting segment.
2. **Focus marketing near commuters traveling under 5 miles**, such as city and suburban areas, and review how to serve long-distance commuters.
3. **Don't segment by gender**; purchase rates are nearly equal.
4. **Look at the Pacific region** to see what drives its higher conversion and whether it can be replicated elsewhere.

**Author: Amir Deldar**

**Contact:**

[LinkedIn](https://www.linkedin.com/in/amirdeldar) · [GitHub](https://github.com/amir-deldar) · Email: <callmedeldar@gmail.com>

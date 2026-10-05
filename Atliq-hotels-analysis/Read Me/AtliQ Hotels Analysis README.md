# AtliQ Hotels: Occupancy, Revenue & Guest Experience Analysis

An end-to-end data analysis of **25 hotel properties across 4 Indian cities** (Mumbai, Bangalore, Hyderabad, Delhi) for May–July 2022. The goal: find where the hotel chain is winning, where revenue is leaking, and what to do about it.

## Key Findings

| Area | Finding |
| --- | --- |
| Demand pattern | Weekend occupancy is **74.0%** vs **51.8%** on weekdays |
| Revenue | **₹170.9 Cr** realized; Mumbai contributes \~39% |
| Occupancy | Delhi leads (61.5%); Atliq Seasons is lowest (44.5%) |
| Cancellations | **24.8%** of bookings cancelled, plus 5.0% no-shows (\~₹30 Cr gap between booked and realized revenue) |
| Ratings | Overall 3.62; Atliq Seasons (2.30) and Grands (3.10) are well below average |
| Channels | Direct bookings bring only \~15% of revenue |

## Recommendations

1. Fill weekdays with corporate tie-ups and midweek packages
2. Run a service audit at Atliq Seasons and Atliq Grands
3. Reduce cancellations with deposits or tighter cancellation windows
4. Grow direct bookings with loyalty offers

## Data

| File | Description |
| --- | --- |
| `dim_hotels.csv` | 25 properties: name, category, city |
| `dim_rooms.csv` | 4 room classes (Standard, Elite, Premium, Presidential) |
| `dim_date.csv` | Calendar with weekday/weekend flag |
| `fact_bookings.csv` | Individual bookings with revenue, status, platform, rating |
| `fact_aggregated_bookings.csv` | Daily capacity and successful bookings per room category |
| `new_data_august.csv` | Additional August records |

## Method

1. Loaded and merged the five core tables with pandas
2. Cleaned the data: removed negative guest counts, revenue outliers (mean + 3 SD) and capacity errors; filled 2 missing capacities with the median
3. Parsed mixed date formats day-first (`dayfirst=True`)
4. Calculated occupancy % = successful bookings ÷ capacity
5. Analysed occupancy, revenue, platforms, cancellations and ratings by city, brand, room class and day type

## Tech Stack

Python · pandas · Jupyter Notebook · PowerPoint

## Repository Structure

```
atliq-hotels-analysis/
├── data/
│   ├── dim_date.csv
│   ├── dim_hotels.csv
│   ├── dim_rooms.csv
│   ├── fact_aggregated_bookings.csv
│   ├── fact_bookings.csv
│   └── new_data_august.csv
├── notebook/
│   └── exercise_solution.ipynb
├── presentation/
│   ├── AtliQ_Hotels_Analysis.pptx
│   └── AtliQ_Recommendation_Slides.pptx
└── README.md
```

## Author

**Hari**: [LinkedIn](https://www.linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)
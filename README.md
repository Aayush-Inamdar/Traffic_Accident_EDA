# 🚦 Urban Traffic Accident Data Analysis

End-to-end exploratory data analysis of 76,000+ real UK road collisions, uncovering accident patterns across time, weather, road type, and driver demographics using Python, Pandas, Matplotlib, and Seaborn.

---

## 📁 Dataset

**Source:** [UK Department for Transport — Road Safety Data 2024](https://www.gov.uk/government/statistics/road-safety-data)

Three official government CSV files merged for analysis:

| File | Rows | Description |
|------|------|-------------|
| `dft-road-casualty-statistics-collision-2024.csv` | 100,927 | Core accident records |
| `dft-road-casualty-statistics-vehicle-2024.csv` | 183,514 | Vehicle-level details |
| `dft-road-casualty-statistics-casualty-2024.csv` | 128,272 | Casualty-level details |

**After merging and cleaning:** 76,575 rows × 72 columns

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data loading, merging, cleaning
- **NumPy** — numerical operations
- **Matplotlib** — custom plots
- **Seaborn** — statistical visualisations
- **Jupyter Notebook** — interactive analysis

---

## 🔧 Setup

```bash
git clone https://github.com/yourusername/urban-traffic-eda
cd urban-traffic-eda

python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

pip install pandas numpy matplotlib seaborn jupyter

jupyter notebook
```

Place the 3 CSV files in the project root, then open `traffic_eda.ipynb`.

---

## 📊 Analysis Overview

### Data Pipeline
```
Load 3 CSVs → Dirty merge → Drop duplicate columns → Remove low-value columns
→ Fix sentinel values (-1 → NaN) → Parse dates → Extract time features → EDA
```

### Plots Generated

| # | Plot | Insight |
|---|------|---------|
| 1 | Accidents by Hour of Day | Rush hour peaks at 8am and 5pm |
| 2 | Accidents by Day of Week | Fridays see the highest volume |
| 3 | Accidents by Month | Seasonal trends across the year |
| 4 | Hour × Day Heatmap | Combined time-of-day risk matrix |
| 5 | Weather Condition Distribution | Most accidents occur in fine weather |
| 6 | Severity by Weather | Fatal accidents cluster in poor conditions |
| 7 | Accidents by Road Type | Single carriageways dominate |
| 8 | Severity by Road Type | Dual carriageways have higher fatal rates |
| 9 | Top 15 Vehicle Models | Most frequently involved makes |
| 10 | Driver Age Distribution | 20s are the highest-risk age group |
| 11 | Accidents by Sex of Driver | Male drivers involved significantly more |
| 12 | Correlation Matrix | Relationships between key variables |

---

## 💡 Key Takeaways

- Accidents peak during morning and evening rush hours, confirming commute-time risk.
- Fridays see the highest accident volume across the week.
- The vast majority of accidents occur in fine weather — simply because more people drive then.
- Single carriageways account for the most accidents by road type.
- Drivers in their 20s are the most frequently involved age group.
- Most accidents are "Slight" in severity, but fatal accidents cluster around high speed limits and poor lighting.

---

## 📂 Project Structure

```
urban-traffic-eda/
│
├── traffic_eda.ipynb                          # Main analysis notebook
├── README.md                                  # This file
│
├── dft-road-casualty-statistics-collision-2024.csv
├── dft-road-casualty-statistics-vehicle-2024.csv
├── dft-road-casualty-statistics-casualty-2024.csv
│
├── plot1_hourly_accidents.png
├── plot2_daily_accidents.png
├── plot3_monthly_accidents.png
├── plot4_heatmap_hour_day.png
├── plot5_weather_distribution.png
├── plot6_severity_by_weather.png
├── plot7_road_type.png
├── plot8_severity_by_road_type.png
├── plot9_top_makes.png
├── plot10_driver_age.png
├── plot11_sex_of_driver.png
└── plot12_correlation_matrix.png
```

---

## 📜 License

Data © UK Department for Transport, licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).

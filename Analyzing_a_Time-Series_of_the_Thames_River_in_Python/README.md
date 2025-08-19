# Time Series Analysis of the Thames River (London Bridge Point)

## 🌊 Project Overview
This project analyzes time series data of the River Thames at the London Bridge tidal gauge point (1890–2000s). The goal is to practice time series exploration, understand autocorrelation, and investigate water level trends to assess flood risks.

### Why It Matters
- Time series analysis is a cornerstone of data science.
- Rising flood risks globally make long-term river monitoring critical for identifying warning signals.

## 🛠️ Tools & Libraries
- **Python**: Core programming language
- **Pandas**: Data wrangling
- **Matplotlib/Seaborn**: Visualization
- **Jupyter Notebook**: Interactive exploration

## 🎯 Goals
- **Primary**: Practice time series analysis with real-world data
- **Secondary**: Learn autocorrelation and time series methods

## 📂 Dataset
- **Coverage**: ~100+ years of Thames river levels
- **Focus**: London Bridge tidal gauge point
- **Columns**:
  - `datetime`: Timestamp
  - `water_level`: Water level in meters
  - `is_high_tide`: 1 = high tide, 0 = low tide
- **Size**: 115,503 rows

## 📊 Key Tasks & Process

### 🔹 Task 1: Data Cleaning
1. Imported raw `.txt` files, fixed pandas import issues
2. Dropped misparsed column (`HW=1` or `LW=0`)
3. Confirmed no null values
4. Renamed columns: `datetime`, `water_level`, `is_high_tide`
5. Fixed dtypes: `datetime` → datetime, `water_level` → float
6. Added `year` and `month` columns
7. Created reusable cleaning function:
```python
def cleaning_data():
    # Automates all cleaning steps
```

### 🔹 Task 2: Initial Exploration
- **Visualizations**:
  - Histograms & boxplots for water level distributions (high vs. low tides)
    - **Low tide**: -2 to -3 m, many upper outliers
    - **High tide**: 3 to 3.7 m, many lower outliers
  - Boxplots outperformed histograms for anomaly detection
- **Summary**: `df.describe()` confirmed ranges
- **Long-term trend**:
  - Counted "very high tide days" (>75th percentile) per year
  - Calculated ratio: very high tide days / all high tide days
  - **Finding**: Dangerous upward trend
    - ~3% (1890s) → ~35% (2000s)
    - 🚨 Indicates rising flood risk in London
  - Low tide trends stable, no significant change

### 🔹 Task 3: Monthly Trends (1927–1929 Flood Disaster Years)
- Created `water_level` dataframe with median monthly values using `.resample('M').median()`
- Plotted trends for 1927–1929 with median reference line
- **Results**:
  - **Low tide**: Spikes in Oct–Dec
  - **High tide**: Spikes in Aug–Nov
- **Insight**: First use of `.resample()` for efficient time series grouping

### 🔹 Autocorrelation Results
Analyzed water level changes over time:
- **Annual**:
  - Low tide: -0.19
  - High tide: -0.23
- **Monthly**:
  - Low tide: -0.36
  - High tide: -0.20
- **Biweekly (15D)**:
  - Low tide: -0.84
  - High tide: -0.74
- **Daily**:
  - Low tide: +0.12
  - High tide: -0.06

**Interpretation**:
- Strong negative autocorrelation biweekly → tides swing oppositely fast
- Weak daily autocorrelation → random day-to-day variation
- Mild negative correlation annually/monthly → long-term cycles, no strong persistence

## 🚀 Key Skills Demonstrated
- Time series data cleaning & wrangling
- Pandas `.resample()` for temporal aggregation
- Exploratory visualizations (histograms, boxplots, time series plots)
- Ratio-based trend analysis
- Autocorrelation interpretation

## 📌 Conclusion
This project showcased time series analysis on Thames River data:
- High tides increasingly extreme: ~35% "very high" days (2000s) vs. ~3% (1890s)
- Low tides stable → imbalance in rising water levels
- Autocorrelation highlights natural tidal cycles (biweekly negative swings)
- `.resample()` is vital for irregular time series summarization

## ⚡ Takeaway
The River Thames shows a dangerous rise in extreme high tides, underscoring the value of time series analysis for climate change and flood risk research.
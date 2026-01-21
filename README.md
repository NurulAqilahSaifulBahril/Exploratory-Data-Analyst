# Exploratory Data Analysis: U.S. Airline Performance Analysis (2015)

## 1. Problem Statement
Flight delays significantly impact customer satisfaction, airline operating costs, and overall system efficiency. 
This project analyzes U.S. flight data from 2015 to identify temporal patterns, airline-level performance differences, 
and operational reliability across major carriers.

The goal is to benchmark airline performance using flight volume and delay behavior, and to identify insights that 
could inform operational improvements and future predictive modeling.

---

## 2. Dataset
- **Source:** Kaggle – U.S. Flight Delay Dataset
- **Time Period:** January–December 2015
- **Size:** ~5.8 million flight records
- **Files Used:**
  - `airlines.csv` (airline codes and names)
  - `flights.csv` (flight-level operational data)

---

## 3. Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 4. Data Preparation
Key preprocessing steps included:
- Handling missing values by removing columns with excessive nulls
- Standardizing categorical variables and column names
- Merging flight and airline datasets using IATA airline codes
- Creating engineered features to classify flights as delayed or on-time

Detailed preprocessing logic is available in the notebook.

---

## 5. Feature Engineering
A new categorical feature, `DELAY_STATUS`, was created based on departure delay:
- **Delayed:** Departure delay > 0 minutes
- **On Time:** Departure delay ≤ 0 minutes

This feature enabled aggregation-based performance analysis across airlines and months.

---

## 6. Exploratory Data Analysis

### 6.1 Trend Analysis
- Monthly flight volumes and delay counts were analyzed to identify seasonal effects.
- Summer months exhibited peak traffic, with disproportionate delays observed in early peak season.

### 6.2 Airline Performance Analysis
- Airlines were benchmarked based on total flights and total delayed flights.
- High-volume airlines demonstrated varying operational reliability.

### 6.3 Correlation Analysis
- The relationship between flight volume and delay rate was assessed at the airline level.
- Results indicate that higher traffic does not necessarily imply higher delay rates, highlighting differences in operational efficiency.

---

## 7. Key Findings
- July recorded the highest flight volume, reflecting peak summer travel demand.
- June experienced a higher number of delays than July, suggesting early-season operational strain.
- Southwest Airlines operated the most flights, indicating strong market presence.
- American Airlines and Delta Air Lines achieved high flight volumes with comparatively lower delay rates, suggesting stronger reliability.

---

## 8. Assumptions & Limitations
- Delay classification is based solely on departure delay, excluding arrival and taxi delays.
- External factors such as weather, airport congestion, and air traffic control constraints were not included.
- Analysis is descriptive and does not include predictive modeling.

---

## 9. Future Work
- Incorporate weather and airport-level congestion data
- Develop a predictive model for flight delays
- Analyze route-level and airport-level performance
- Extend analysis to multiple years for trend stability

---

## 10. Reproducibility
1. Clone the repository
2. Install required Python packages
3. Run the provided Jupyter notebooks in sequence

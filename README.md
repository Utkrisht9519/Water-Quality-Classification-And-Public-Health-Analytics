# Water Quality Classification Project

## Problem Statement
Water quality monitoring is critical for public health and environmental sustainability. 
This project aims to analyze water quality data collected from monitoring stations in Maharashtra and build machine learning models to classify water into different quality categories (Class A–E) based on physicochemical parameters.

The objective is to:
- Understand key factors affecting water quality
- Perform exploratory data analysis (EDA)
- Build and evaluate classification models
- Identify the most suitable model for water quality prediction

---

## Dataset Description
- **Source:** Maharashtra Pollution Control Board (MPCB)
- **File:** `NWMP_August2025_MPCB_0.csv`
- **Granularity:** Individual water samples
- **Target Variable:** `Water_Class`

### Key Features Used
- pH
- Dissolved Oxygen (DO)
- Biochemical Oxygen Demand (BOD)
- Chemical Oxygen Demand (COD)
- Total Dissolved Solids (TDS)
- Turbidity

Each row represents a water sample with measured environmental parameters.

---

## Key Findings (EDA)
- Water quality classes are **imbalanced**, with Class A appearing most frequently.
- Higher BOD and COD values are associated with poorer water quality.
- Dissolved Oxygen (DO) is a strong indicator of cleaner water.
- Several features show overlapping distributions, making classification non-trivial.

---

## Model Performance
Three models were evaluated:

### Logistic Regression
- Strong bias toward the majority class
- Failed to identify minority classes effectively
- Served as a baseline model

### Random Forest (Best Model)
- Learned non-linear relationships
- Improved minority-class detection
- Achieved the highest mean cross-validated macro F1-score
- Provided the best balance between stability and performance

### Extra Trees
- Performance similar to Random Forest
- Slightly lower mean F1-score
- Confirmed that model performance is now data-limited

**Selected Model:** Random Forest

---

## Project Structure

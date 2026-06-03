# Ironman 70.3 Performance Analysis
## Capstone Project — UC Berkeley ML/AI Professional Certificate

### Overview
This project analyzes over 821,000 amateur finisher records from Ironman 70.3 
races worldwide between 2004 and 2020. The goal is to predict an athlete's 
finish time based on demographic information and partial race splits, and to 
identify which race segment has the greatest impact on overall performance.

### Research Questions
1. Can we predict the finish time of an amateur athlete in an Ironman 70.3 
   based on their swim and bike splits?
2. Which race segment — swim, bike or run — has the greatest predictive 
   power over the final finish time?
3. Has the average performance of amateur athletes improved between 2004 
   and 2020?
4. How does performance vary across age groups, and in which segment does 
   it decline fastest with age?

### Dataset
- **Source:** [Kaggle — Ironman 70.3 Race Data 2004-2020](https://www.kaggle.com/datasets/aiaiaidavid/ironman-703-race-data-between-2004-and-2020)
- **Records:** 821,099 amateur finishers (after cleaning)
- **Features:** Gender, AgeGroup, Country, EventYear, EventLocation, 
  SwimTime, BikeTime, RunTime, Transition times, FinishTime
- **Target:** FinishTime (minutes)

### Data Cleaning
- Removed 16,611 professional athlete records (AgeGroup = '00')
- Removed 2,365 records exceeding the official 8h30min race cutoff
- Final dataset: 821,099 clean amateur records

### Key EDA Findings
- Average finish time: 354 minutes (5h54)
- Gender gap: men finish ~28 minutes faster than women, mostly on the bike
- Run is the segment that deteriorates fastest with age
- Average finish times have remained stable between 2004 and 2020
- Bike and run times show the highest correlation with finish time (0.87 and 0.89)

### Modeling Approach
The models predict finish time using swim and bike splits as features, 
simulating a mid-race scenario where an athlete has completed two segments 
and wants to estimate their final result.

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Baseline (demographics only) | 37.85 min | 47.11 min | 0.09 |
| Linear Regression | 15.48 min | 20.16 min | 0.83 |
| Ridge Regression | 15.48 min | 20.16 min | 0.83 |
| Random Forest | 15.43 min | 20.09 min | 0.83 |
| **Gradient Boosting** | **15.28 min** | **19.90 min** | **0.84** |

### Key Modeling Findings
- Bike time is by far the strongest predictor (feature importance: 0.88)
- Adding segment times improved R² from 0.09 to 0.84
- The relationship between splits and finish time is largely linear
- Gradient Boosting is the best model with MAE of ~15 minutes

### Repository Structure

## Project Structure

```
├── data/
│   └── ironman_703.csv        # Raw race data
├── notebooks/
│   └── ironman_capstone.ipynb # Main analysis notebook
├── README.md
└── requirements.txt
```

### Requirements

pandas
numpy
matplotlib
seaborn
scikit-learn

## Setup

```bash
pip install -r requirements.txt
```

### Author
Angel Barbancho Sanchez
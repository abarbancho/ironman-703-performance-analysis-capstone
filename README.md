# Ironman 70.3 — Performance Analysis

Analysis of Ironman 70.3 race data including swim, bike, and run splits.


## Research question

Can we predict the finish time of an amateur athlete in an Ironman 70.3 race based on their age, sex, country of origin, and race location, and which race segment — swim, bike, or run — has the greatest predictive power over the final result?

Expected data source

Kaggle dataset: Ironman 70.3 races 2004–2020, containing 823,464 finisher records across 197 events in 183 locations worldwide. Variables include sex, age group, country of origin, event location, year, and split times for swim, bike, run, and transitions.

https://www.kaggle.com/datasets/aiaiaidavid/ironman-703-race-data-between-2004-and-2020Links to an external site.

## Techniques

Exploratory Data Analysis (EDA) to understand distributions across age groups, sex, and geography.
Regression models (Linear Regression, Ridge, Decision Tree Regressor) to predict finish time.
Feature importance analysis to identify which segment and athlete characteristic contributes most to the final time.
Time series analysis to explore performance trends between 2004 and 2020.
Model comparison using MAE and R² as evaluation metrics.
Expected results

I expect to build a regression model that can predict an athlete's finish time with reasonable accuracy. I anticipate that the bike segment will show the highest raw correlation with finish time due to its length, but that the run segment may emerge as a stronger relative predictor — especially in older age groups where running performance tends to decline faster. I also expect to find a gradual improvement in average finish times over the 16-year period, likely driven by advances in training methodology and equipment.

## Why this question is important

Every year hundreds of thousands of amateur athletes around the world sign up for Ironman 70.3 races. Most of them are not professional athletes — they are regular people balancing training with work and family, trying to make the most of the limited time they have to prepare. One of the most common questions any triathlete asks is: where should I focus my training to improve my overall time?

Right now, most athletes rely on generic advice or personal intuition to answer that question. This project aims to provide a data-driven answer — one that accounts for the athlete's age, sex, and the specific race they are targeting. The results could help amateur triathletes and their coaches make smarter decisions about where to invest training time, and give race organisers a clearer picture of how participation and performance have evolved over nearly two decades of the sport.

If this question goes unanswered, athletes continue making training decisions based on assumptions rather than evidence. A model that identifies the most impactful segment by age group and sex turns a complex dataset into practical, personalised guidance that any athlete can understand and act on — no machine learning knowledge required.

## Project Structure

```
├── data/
│   └── ironman_703.csv        # Raw race data
├── notebooks/
│   └── ironman_capstone.ipynb # Main analysis notebook
├── README.md
└── requirements.txt
```

## Setup

```bash
pip install -r requirements.txt
```


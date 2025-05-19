# NBA PPG Prediction with Linear Regression

This project builds a linear regression model to predict NBA players' points per game (PPG) using their per-game statistics such as field goals, minutes played, and free throw attempts. The model is not discovering a hidden pattern, but reconstructing a known relationship. Built in Python using pandas, scikit-learn, and matplotlib. 

---

## Project Summary

-**Goal**: Predict ppg using other in-game stats
-**Approach**: Feature selection ->  Linear regression -> Evaluation -> Visualization
-**Data**: Player per game stats from 2025 NBA season from https://www.kaggle.com/datasets/sumitrodatta/nba-aba-baa-stats/discussion/563692

---

## How to Run

1. Clone the repo
    git clone https://github.com/justinvuong/nba-ppg-regression.git
    cd nba-pp-regression
2. Create and activate virtual environment (Optional)
    python -m venv nba-env
        This creates a folder named nba-env/ containing an isolated Python environment
    nba-env\Scripts\activate
        Once activated, your prompt should show something like: (nba-env) C:\your\path
3. Install dependencies
    pip install -r requirements.txt
4. Launch the notebook 
    jupyter lab

---

## Key Features Used

-`g` - games played
-`mp_per_game`, `fga_per_game` - field goals made/attempted
-`x3p_per_game`, `x3pa_per_game` - 3-point shots made/attempted
-`ft_per_game`, `fta_per_game` - free throws made/attempted
-`trb_per_game` - total rebounds
-`ast_per_game` - assists
-`tov_per_game` - turnovers

*Percentage-based stats were intentionally excluded to avoid misleading model signals.*

---

## Model Performance

R^2 Score (Coefficient of Determination): 0.9999
    This measures how well the model's prediction match the actual data. A score of 1.0 = perfect fit, 0.0 = model predicts no better than the mean.
RMSE (Root Mean Squared Error): ~0.075
    This measures average prediciton error in the same units as the target (pts_per_game). A lower RMSE = more accurate predictions.    

---

## Visualization

![Actual vs Predicted PPG](output/actual_vs_predicted_ppg.png)

> A tight scatterplot around the y-x line shows strong model accuracy. 


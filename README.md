FIFA Players Rating Analysis & Prediction (2015-2021)
Project Overview

This project analyzes FIFA player data from 2015 to 2021, tracks player rating progression, evaluates club performance trends, and builds a machine learning model to predict FIFA 21 player ratings. The analysis helps understand player development and can support scouting and recruitment decisions.

Dataset

Source: FIFA datasets (2015–2021)

Format: CSV files for each FIFA year

Key Features:

Player attributes: pace, shooting, passing, dribbling, defending, physic, age

Goalkeeper attributes: gk_diving, gk_handling, gk_kicking, gk_reflexes, gk_speed, gk_positioning, age

Player information: sofifa_id, short_name, club_name, player_positions, potential, overall

Steps Performed

Data Loading and Cleaning

Loaded datasets for FIFA15 to FIFA21.

Merged all datasets into a single DataFrame with consistent player IDs and FIFA version.

Removed unnecessary columns, handled missing values, calculated BMI and potential increase.

Exploratory Data Analysis (EDA)

Analyzed average overall rating per year.

Tracked top players such as Messi and Ronaldo across editions.

Visualized rating distributions and club performance trends.

Examined potential growth for players.

Machine Learning Modeling

Algorithm: Random Forest Regressor

Separate models were built for field players and goalkeepers.

Features were scaled using StandardScaler.

Data split into training and testing sets (80/20) and model trained with 200 trees.

Evaluation metrics included R² and RMSE.

Prediction and Evaluation

Predicted FIFA 21 ratings for all known players.

Achieved high accuracy:

Field Players: R² = 0.95, RMSE ~1.72

Goalkeepers: R² = 0.92, RMSE ~2.15

Overall: R² ≈ 0.94, RMSE ~1.87

Visualizations

Average overall ratings per year.

Rating progression of selected players.

Distribution of ratings per FIFA edition.

Top club performance trends.

Average potential increase over the years.

(Plots generated using Matplotlib and Seaborn.)

Tools and Libraries

Python 3.x

Pandas and NumPy (data processing)

Matplotlib and Seaborn (visualization)

Scikit-learn (Random Forest, scaling, train/test split)

FPDF (PDF report generation)

Key Insights

Player ratings gradually evolve over the years, with top players maintaining high and stable ratings.

Leading clubs consistently perform at a high level.

Random Forest model accurately predicts FIFA 21 ratings.

The analysis can be useful for scouting and player recruitment.

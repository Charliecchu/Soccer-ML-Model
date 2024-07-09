# Bundesliga Match Outcome Predictor
This project uses a machine learning model to predict the outcome of Bundesliga matches based on historical data.

## Overview
The script employs a RandomForestClassifier from the sklearn.ensemble module to predict football match outcomes. Key features extracted include venue, opponent, match timing, and historical head-to-head performance metrics. The dataset is created by webscraping https://fbref.com/en/. 

## Getting Started
### Prerequisites
Before running the script, make sure to install the following Python packages:

pandas
scikit-learn
You can install these packages using pip:

pip install pandas scikit-learn

### Dataset
The dataset should be a CSV file with the following columns:

* date
* venue
* opponent
* time
* result
* team
* referee
Other match statistics (goals for, goals against, shots, shots on target, etc.)

### Running the Code

Load the script into your Python environment and execute it. Ensure the dataset Bundesliga_Matches.csv is present in the same directory as the script or provide the correct path to the file.

## Functions
* h2h_performance(matches): Calculates historical head-to-head average goals for and against for each match.
* rolling_averages(group, cols, new_cols): Computes rolling averages for specified columns over the last three matches.
* make_predictions(data, predictors): Trains the RandomForestClassifier and makes predictions on the test dataset.

## Features
The features used for prediction are:

* Venue number
* Opponent number
* Match hour
* Day of the week
* Historical head-to-head performance
* Rolling averages of match statistics (goals, shots, distance, etc.)
* Referee number

## Model Performance
The script outputs the accuracy and precision of the model predictions on the test dataset. It provides insights into the performance of the model when tested with unseen data.

## Notice
* The model uses a random state for reproducibility; however, changing the random state can lead to different results.
* The cutoff date for training and testing is set to '2024-01-01'. Adjust this date based on the data available and the desired testing period.

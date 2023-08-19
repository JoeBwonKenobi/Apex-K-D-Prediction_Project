# Apex K/D Prediction_Project
 Predicting future K/D Ratios for Apex Legends

Project objective: construct a model to predict Kills and deaths in Apex Legends

I obtained data directly from the in-game stats and made it into a dataframe so that I could visualize and prepare the data for modeling

I preformed feature engineering to create more columns using the existing data. Here's a list of columns and how they were created:

- Top 5% - Divided the Total Top 5 Finish column by the Total games played column.

- Kill/Knock Ratio - Divided The Total kills column by the knockdowns column.

- Average knocks per game - Total games played divided by knockdowns column.

- Average assists per match - Divided Assists column by total games played.

- Average damage per match- Total damage divided by total games played.

Here are some overall career statistics about the data:

- The average number of total kills per season is: 389
- The average total damage per season overall is: 180922
- The average number of total top 5 finishes per season is: 162

%%html



Linear Regression model

The model's performance on the training data is remarkably accurate, perfectly predicting outcomes. For the testing data, the model performs very well too, explaining most of the variability in predictions, with only minor discrepancies between predicted and actual values.

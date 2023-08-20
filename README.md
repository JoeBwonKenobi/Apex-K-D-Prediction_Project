# Apex K/D Prediction_Project
 Predicting future K/D Ratios for Apex Legends

# **Project objective:**
- Visualize trends throughout seasons, and construct a model to predict Kills a death ratio in Apex Legends.

# **Methods**

I obtained data directly from the in-game statistics and made it into a dataframe so that I could visualize and prepare the data for modeling.

I preformed feature engineering to create more columns using the existing data. Here's a list of columns and how they were created:

- Top 5% - Divided the Total Top 5 Finish column by the Total games played column.

- Kill/Knock Ratio - Divided The Total kills column by the knockdowns column.

- Average knocks per game - Total games played divided by knockdowns column.

- Average assists per match - Divided Assists column by total games played.

- Average damage per match - Total damage divided by total games played.

Here are some overall career statistics about the data:

- The average number of total kills per season is: 389
- The average total damage per season overall is: 180922
- The average number of total top 5 finishes per season is: 162

# **Visualizations**

## **Average Knocks Per Game/ K/D Ratio by season**

- This is an overall good measurement for gauging improvment throughout the seasons as far as getting knocks(downing another player in the game).
- The 'R' stands for Ranked, a separate more competeive game mode, the stats for the ranked season are included in the season as a whole.

  
![AVERAGE KNOCKS](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/626568d0-90f8-4910-9b42-aaa09d64d414)


## **Average Damage / Total Top 5 Per season**

- This is also an overall good measurement for gauging improvement throughout the seasons because it shows a comparison of Average damage per match and number of top 5 finishes in a seson. If these are both improving then not only I am a getting more damage per match on average, but I'm also finishing in the Top 5 more often which should ultimately mean more wins, knocks, and kills overall.

  
![Average Damage- Total Top 5](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/b23182b1-81a2-4e59-9d98-f06e51b82371)



## **Average Revives / Respawn Per match**

- This shows the average amount of revives and respawns per match by season. This is in a way a good measure of being a good teamate, but also a measure of how goo/bad my teamates are, which most of the time is comletely out of my control.



![Average Revive - Respawn](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/4c3a1d54-159a-4302-ae1d-1114a2429759)


Linear Regression model

The model's performance on the training data is remarkably accurate, perfectly predicting outcomes. For the testing data, the model performs very well too, explaining most of the variability in predictions, with only minor discrepancies between predicted and actual values.

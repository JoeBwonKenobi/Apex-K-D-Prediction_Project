# Apex Kill/Death Prediction Project
 Predicting future K/D Ratios for Apex Legends
 


<img src="https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/e1168bbb-48b7-4e49-91fc-e7a20b4af394" alt="Apex Legends" width="100%">
*I do not own this photo*

# **Project objective:**
- Visualize trends throughout seasons, and construct a model to predict Kills to death ratio in Apex Legends.

## **About Apex Legends:**

Apex Legends is an extremely fast-paced, free-to-play battle royale game set in the Titanfall universe. In this highly competitive online multiplayer game, players are grouped into squads of three, each controlling a unique character known as a "Legend." The objective is to be the last squad standing among 20 squads on a constantly shrinking map.

Players jump into the game from a dropship, and once on the ground, they scavenge for weapons, equipment, and resources to survive. During combat, if a player takes substantial damage, they can be "knocked down." This means they are temporarily incapacitated and can only crawl on the ground. Teammates can revive knocked players, but if not rescued in time, they may bleed out or be killed. The game's dynamics involve a blend of gunplay, strategic positioning, and effective use of each Legend's unique abilities to secure victory.

The shrinking play area forces intense encounters and strategic decisions as squads fight to eliminate each other. The ranked version of the game is esentailly the same only with a score provided at the end of each match that coralates with a point system to assign the player a rank. At the end of a given season, a player may recieve rewards based on their preformance in "Ranked" that can be visable to other players. Apex Legends is known for its diverse cast of Legends, each with their own special abilities that add layers of tactics and team synergy to the gameplay. It continues to evolve with regular updates, making it a dynamic and engaging battle royale experience. There is a collection of the players preformance data in-game provided to the player simply by loading into the main game lobby and clicking on their avatar.

# **Methods**

I obtained data directly from the in-game statistics and transformed it into a dataframe so that I could visualize and prepare the data for modeling.

I preformed feature engineering to create more columns using the existing data. Here's a list of columns and how they were created:

- Top 5% - Divided the Total Top 5 Finish column by the Total games played column.

- Kill/Knock Ratio - Divided The Total kills column by the knockdowns column.

- Average knocks per game - Total games played divided by knockdowns column.

- Average assists per match - Divided Assists column by total games played.

- Average damage per match - Total damage divided by total games played.

Here are some overall career statistics about the data:

- The average number of total kills per season overall is: 389
- The average total damage per season overall is: 180922
- The average number of total top 5 finishes per season overall is: 162
  
# **Visualizations**

## **Average Knocks Per Game/ K/D Ratio by season**

- This is an overall good measurement for gauging improvment throughout the seasons as far as getting knocks(downing another player in the game).
- The 'R' stands for Ranked, a separate more competeive game mode, the stats for the ranked season are included in the season as a whole.



![AVERAGE KNOCKS](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/5db5a0e8-e3dd-4e87-a73a-9ab5582e8115)





## **Average Damage / Total Top 5 Per season**

- This is also an overall good measurement for gauging improvement throughout the seasons because it shows a comparison of Average damage per match and number of top 5 finishes in a seson. If these are both improving then not only I am a getting more damage per match on average, but I'm also finishing in the Top 5 more often which should ultimately mean more wins, knocks, and kills overall.



![Average Damage- Total Top 5](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/8ceaabd7-bfb4-49a4-bf41-20c0b9cf8203)

 


## **Average Revives / Respawn Per match**

- This shows the average amount of revives and respawns per match by season. This is in a way a good measure of being a good teamate, but also a measure of how goo/bad my teamates are, which most of the time is comletely out of my control.



![Average Revive - Respawn](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/2cfa752a-e402-4302-a6b4-cc13809f3c00)

- These visuals give insight about some of the aspects of the game and my progress throughout the seasons. There are several others available on my tableau public profile.

# **Model analysis**

Linear Regression model
I used a linear regression model to predict the number of kills in a season. The R2 score gauges how well the model predicts what it was built to predict.
I recived the following results upon running the model:

![Apex linear Model](https://github.com/JoeBwonKenobi/Apex-K-D-Prediction_Project/assets/117705408/d488882b-04f9-4cdb-9546-297c90376a9c)


The model's performance on the training data is remarkably accurate, perfectly predicting outcomes. For the testing data, the model performs very well too, explaining most of the variability in predictions, with only minor discrepancies between predicted and actual values. This model is excellent at predicting the amount of kills in a season of Apex Legends. 

# **Project Conclusion**

There are a large amount of things to consider when predicting something like a k/d for a season worth of play, especially with a game like apex that constantly updates, has an unpredictable amount of players at different times of the day that have an unpredictable amount of skill for the match I would hypothetically face them in. There are many other factors to consider, but the purpose of this project was to make preictions based on the data provided.

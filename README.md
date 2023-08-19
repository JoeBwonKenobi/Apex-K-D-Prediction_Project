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
<div class='tableauPlaceholder' id='viz1692412847216' style='position: relative'><noscript><a href='#'><img alt='K&#47;D Ratio Per Season ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ap&#47;Apex_KDRatio_Visual&#47;Sheet1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Apex_KDRatio_Visual&#47;Sheet1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ap&#47;Apex_KDRatio_Visual&#47;Sheet1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1692412847216');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>


Linear Regression model

The model's performance on the training data is remarkably accurate, perfectly predicting outcomes. For the testing data, the model performs very well too, explaining most of the variability in predictions, with only minor discrepancies between predicted and actual values.

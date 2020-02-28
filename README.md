# Predicting Impressions from Political Ads from Snapchat data in 2019
## Determining Impressions from Duration
![Picture1](https://user-images.githubusercontent.com/60996310/75574690-bf22a100-5a2c-11ea-8a9f-6ed885f046d6.png)
It makes sense for duration and impressions to be directly related as the longer the duration, the higher the exposure, and the higher the familiarity and impressionableness. It's not the case in this scenario as it seems that longevity of the time that the ads run have no effect on the number of impressions. This is a highly poor measure of future impressions as the rsq value is not even 1% meaning barely 1% of the durations data can explain/predict future impressions. We would need a different variable to better explain and improve methods to increase impressions.
## Determining Impressions from Spending and Duration
![Picture1](https://user-images.githubusercontent.com/60996310/75576864-c21e9100-5a2e-11ea-8cd9-38e4ce387692.png)
With the amount spent on ads and duration data, it's clear that this data is a better indicator of future impressions. In most of the scenarios, as spending on an ad increases, so does the number of impressions. our Rsq value implies that 74% of the spending data can explain and predict impressions in the future year(s). 

### Excel Steps
1. Import 2019 Political Ads data
2. Delete any noncontributing variables (ie. billing address, url)
3. Filter all columns. Set impressions to descending order. 
4. Split start/end date cells. Data - text to columns - deliminate - "space" as deliminater - do not show column with times.
5. In a new cell, set =datedif(start date, end date, "d") and label the column "Duration_Days"
6. Use Duration (x-value) column and Impressions (y-value) column to create a scatterplot.
7. Obtain the slope (=slope(impressions, duration), yint (=intercept(impressions, duration), and rsq (=RSQ(impressions, duration) values.
8. Click on Data Analysis and Regression. Use Impressions data as y-input values and both Duration and Spending as x-input values by clicking on corresponding cells. Output range is an empty cell. 
9. Obtain regressions data. 

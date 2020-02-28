# Predicting Impressions from Political Ads from Snapchat data in 2019
The demographics are Snapchat users in the Canada and the US as both regions have the highest impressions.
## Determining Impressions from Duration
![Picture1](https://user-images.githubusercontent.com/60996310/75574690-bf22a100-5a2c-11ea-8a9f-6ed885f046d6.png)
It makes sense for duration and impressions to be directly related as the longer the duration, the higher the exposure, and the higher the familiarity and impressionableness. It's not the case in this scenario as it seems that longevity of the time that the ads run have no effect on the number of impressions. This is a highly poor measure of future impressions as the rsq value is not even 1% meaning barely 1% of the durations data can explain/predict future impressions. We would need a different variable to better explain and improve methods to increase impressions.
## Determining Impressions from Spending and Duration
![Picture1](https://user-images.githubusercontent.com/60996310/75577899-eb402100-5a30-11ea-852e-ed5adc55067e.png)
With the amount spent on ads and duration data, it's clear that this data is a better indicator of future impressions. In most of the scenarios, as spending on an ad increases, so does the number of impressions. Our Rsq value implies that 74% of the spending data can explain and predict impressions in the future year(s). This is a better model to fit our data, but it still isn't ideal. We would need more data such as demographics to better appeal to the audience and boost impressions. We would also need to consider each company's budget as spending appears to be a contributing factor in success. There needs to be more qualitative data to see trends. 
In further analysis with a Pivot Table, it also appears that General Mills is the most successful organization in generating a high number of impressions reaching 64M.

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
10. Create Pivot Table with Organization name and Impressions. Name is the rows and Impressions is the value. 

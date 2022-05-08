# Order volume Predictor 
Summary: One of Kepler's clients, Shazamazon, is an eCommerce retail store selling custom-made thingamabobs. Kepler's media team has been tasked with driving more Shazamazon orders to help them get a bigger foothold in the market. But before we start spending our client's money on advertising, we want to better understand what sorts of customer behaviors drive order volume so that our media team can target the most impactful parts of the customer journey.

 

At Kepler's request, Shazamazon provided the attached data set showing daily order volume across each of their target regions, along with the number of emails customers have opened, the average purchase value for each order, the number of social media likes, and the number of website visits. Despite being a retail provider, Shazamazon has confirmed that they never see seasonal variations in order volume, nor do they see any meaningful difference across regions.


1. Your final model equation: not applicable used a GradientBoostingRegressor model
2. model prediction based on the info bellow was 953.93
- date = 2021-01-15
- region_id = 7
- email_opens = 10449
- avg_order_value = 48.02
- social_likes = 447
- total_site_visits = 282887

3. A high-level, step-by-step explanation of how you developed your model and why you took that step: 
- First I read in the data, I had to split up the data by tabs because it was a tsv file
- Second I did some analysis on the data to get a better feel for the data, see if there is any missing data, take a look at the data and see if I needed to deal with catagorical data, and graph out the data and check for any outliers or needed data menipulation. I also relized that avg_order_value and social_likes where random noise so I removed it.
- Next I split up the training set and the test set so I would not over fit the model
- Then I scaled the data so it would be easier for the model to fit
- Next I look a list of models and used cross validation to test there preformance and chose two to try and imporve there results using feature engeneering and hyperperamitor tuning
- After I picked two good looking models I did some feture engeneering and created a new feature using total_site_visits and email_opens, I also turned total_site_visits and email_opens to log form.
- After that I optimized some of the peramitors using grid search and compaired the two final models and chose one
- Then I tested the model on the test set and see how it did
4. I chose this model because it had the best cross validation results and is most likely to do well on out of sample data.
5. Optionally, any other information or visuals that you think help explain the model. If I had to put this model into production I would spend some time converting the code from a note book into pycharm then creating test for all functions and making sure everything was commented well.

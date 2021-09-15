# Neural_Network_Charity_Analysis

## Overview of the analysis:
Using Neural Networks, the goal of this project is to analyze a dataset comprised of chariy data. We use a Neural Network to create a binary classifier that is capable of predicting whther applicants will be successful if funded by Alphabet Soup. The data comes in the form of a csv that is comprised of 34,000 organizations that have received funding from Alphabet Soup in the past. 

The dataset columns are as follows:
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively
- What You're Creating


## Results:
In our first attempted at producing this model, we removed both EIN and NAME column because we assumed that these points weren't going to be useful since our aim is not to pinpoint certine individuals but identify the trend overall. We grouped our most common application types which are the following; T3, T4, T5, T6, T7, T8, T10, and T19.  Since we had such a large data set we ended up with two layers, 80 nodes in the first layer and 30 in the second layer. Increasing the number of epochs only generated marginal improvments so we felt that we had hit the sweet spot as far as that was concerend. Being that this is such a large dataset we had to be efficent with our runs as they could take time to run on weaker machines with no added benefit. For our first attempt we acheived an accuracy score of 72% using a random forest model as it's tends to be the best method for classification problems. It was good, but could definantly be better. 

![attempt 1](https://user-images.githubusercontent.com/78940625/132143736-58241832-3fcb-411e-8cb8-e4809df345d1.PNG)

To improve our model we went back and thought of ways to increase our accuracy score. In our intial phases of creating model we already knew that the number of nodes per layer was already at an optiumum level and so was the number of layers. We did not want to increase them as that would likely lead to overfitting. Instead we looked at our columns and thought about whether including the name column to give our model the ability to group our results so we changed NAME into a datapoint format and filtered in only those who applied for then 5 times in the past. After we ran the model and we were able to acheive a score of 78.8%.

![attempt 2](https://user-images.githubusercontent.com/78940625/132144395-e1392f86-b19e-475f-8004-9045d0c22793.PNG)


## Summary

With a score of 78.8% we can say that our model can accuratly predict the success of Alphabet's donations. By using the NAME column and grouping them into those who have applied more then 5 times. Binning our CLASSIFCATION column into those which are greater then 1000 count, and then using a Random Forest model using Relu and Sigmoid we were able to acheive our best results. 

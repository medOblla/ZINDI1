This is the first place solution for the [Womxn in Big Data South Africa: Female-Headed Households in South Africa Challenge.](https://zindi.africa/competitions/womxn-in-big-data-south-africa-female-headed-households-in-south-africa) 

Go to Zindi to download the data. 

The objective of this challenge was to build a predictive model that accurately estimates the % of households per ward that are female-headed and living below a particular income threshold by using data points that can be collected through other means without an intensive household survey like the census. 

Read more aboout the winners [here](https://zindi.africa/blog/meet-the-winners-of-the-womxn-in-big-data-south-africa-female-headed-households-in-south-africa-challenge).

**Zindi handle:** [Ansem_chaieb](https://zindi.africa/users/Ansem_Chaieb)

**Where are you from?** Tunisia

**Feature engineering:**

I started by dropping features that were the same {'dw_00','dw_02', 'dw_06','dw_12','dw_13','psa_02' ..}. I found that they were not really useful.
I clustered geolocation coordinates to get 5 clusters, then for each cluster I measured the percentage of poverty using the features most correlated with the target.
I tried Binarization and Rounding (it often makes sense to round off these high precision percentages into numeric integers)and some meaningful feature encoding. I also tried to find interactions between features but that did not work.

**Modeling:**

I trained a single LGBM model with 5-fold cross-validation. In order to improve my results and to reduce overfitting to training data, I used model stacking.
What were the things that made the difference for you that you think others can learn from?

Trying to understand the subject you are working on is the most important part. It will help you design your features well. Not all of your assumptions will be good, so keep trying until you get the best result.

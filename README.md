# Will the customer accept a coupon?
## Summary
This exercise takes a dataset from UCI Machine Learning repository for  “Will a customer accept the coupon?”. The goal is to analyze the data, understand how to clean up the data (where applicable), identify patterns and present analysis results through visualizations and probability distributions.

## Findings
### Data quality
#### Nulls
The data quality is generally high for the 12K+ rows in the dataset. There were a few columns that were not complete. In particular these were:
- Car

and visit columns:

- Bar
- CoffeeHouse
- CarryAway
- RestaurantLessThan20
- Restaurant20To50

For 'Car', majority of the data was null for that column and for what was present, it was mostly unusable. So it made sense to drop it.

For the visit columns, it made sense to replace the nulls with 'never'. As in never visited as a representation of nulls.

#### Acceptance ratio
The acceptance ratio was split 57% ('right away') to 43% ('no, I do not want the coupon').

### Bar visitor's coupon acceptance analysis
Various combinations of datasets have been compared to see if any specific factor stands out for Drivers who accepted the Bar coupon. After various sets of distribution analysis were compared, the clear winner was anyone who visited Bar more than once were highly likely (about 70% probability) to accept the Bar coupon.

### Independent analysis
Similar excersises were then made to compare similarity for Coffee House and RestaurantLessThan20 vistors. Coffee House visitors displayed a similar acceptance as Bar visitors (visit count > 1). 

However, RestaurantLessThan20 visitors were likely accept Restaurants<20 coupons even if they visited only once.

## Next steps and recommendation
There are many attributes/features that have not yet been explored in terms of what can drive the acceptance of the coupon.  A few areas that might be worth further exploring:
1. How does the time of the day and destination affect the acceptance? Would morning drivers heading to 'Work' choose to accept a coupon - especially if it has an 'expiration' of '2h'?
2. what factors contribute to accepting a coupon with 2h expiration time?
3. Would drivers with a 'destination' of 'No Urgent Place' have a higher probability of accepting a coupon than otherwise.
4. Do different types of 'weather' bring higher acceptance to certain types of coupons?

Understanding these correlations and probabilities will help improve the acceptance rate of coupons.

## Data citation
In-vehicle coupon recommendation. (2020). UCI Machine Learning Repository. https://doi.org/10.24432/C5GS4P.

## Link to notebook
Here is the [link](prompt.ipynb) to the notebook
# Will the customer accept a coupon?
## Link to notebook
Here is the [link](prompt.ipynb) to the notebook

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

## Data citation
In-vehicle coupon recommendation. (2020). UCI Machine Learning Repository. https://doi.org/10.24432/C5GS4P.
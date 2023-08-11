Created: 2022-11-10 08:11:75
Tags: #ML #DataScience #category_encoder #feature_processing 

## Note
This is the simplest encoder you can use to encode categorical variables.

It works pretty cool. LE just encode categories with order of numbers and encode previously unseen categories with "-1".

*Also, we use it to encode target variable and* ***we can use it if we are encoding features for [[gradient boosting|gradient boosting algorithms]] and set a variable type as "category".***

## References
- [Medium Post](https://towardsdatascience.com/benchmarking-categorical-encoders-9c322bd77ee8)
## Zero Links
- [[Wiki/ml/encoders/Category Encoders|Category Encoders]]
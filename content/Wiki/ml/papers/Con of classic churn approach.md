Created: 20221011161012
Tags: #churn #uplift #ML #DataScience 

## Note
### The Main idea
Instead predict churn ***we should predict the effect from treatments***.

### Description
If we find potential churn clients and then persuade them not to churn these clients will end up in our training dataset as active (not churn) users. Retraining the model will result them to get a lower score. Thus we learn to stop calling persuadable (see [[Wiki/ml/papers/Uplift users|Uplift users]]) customers.

Now imagine that we call people with a high scor and not persuade them. They called lost causes. The model after retrain give them higher score. Thus we learn to keep calling lost causes customers.

Solution

## References
- [Preventing churn like a bandit](https://medium.com/bigdatarepublic/preventing-churn-like-a-bandit-49b7c51b4929)

## Zero Links
- [[Wiki/ml/papers/Churn|Churn]]
- [[Wiki/ml/papers/Uplift|Uplift]]

## Links


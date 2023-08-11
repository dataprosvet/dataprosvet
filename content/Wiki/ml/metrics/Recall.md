Created: 2022-11-02 20:11:09
Tags: #ML #DataScience #classification_metric #ml_metrics

>[!WARNING]
>For understanding recall score you need to read [[Wiki/ml/metrics/Confusion Matrix|Confusion Matrix]] note firstly.
## Note
*Recall* uses to evaluate classification [[machine learning]] algorithm. It has more stability with imbalanced data then [[Wiki/ml/metrics/Accuracy score|Accuracy score]].
![[Files/Precisionrecall.svg.png|400]]

### Definition
- *Recall* is the fraction of relevant instances that were [[retrieve|retrieved]]. In other words how many relevant itemswere [[retrieve|retrieved]]?.
$$Recall=\frac{TP}{TP + FN}$$
### Probabilistic interpretation
- *Recall* is the estimated probability that a document randomly selected from the pool of relevant documents is [[retrieve|retrieved]].
>[!INFO]
>Relevant element (document) is the element (document) has a positive class label.

### Advantages 
- Good works with imbalanced data
- Easy interpretable

## Related metrics
- [[Wiki/ml/metrics/Precision|Precision]]
- [[Wiki/ml/metrics/F measure|F measure]]
- [[Wiki/ml/metrics/Accuracy score|Accuracy score]]
- [[Balanced accuracy score]]

## References
- [Precision and recall from Wikipedia](https://en.wikipedia.org/wiki/Precision_and_recall)
## Zero Links
- [[Wiki/ml/metrics/Classification Metrics|Classification Metrics]]
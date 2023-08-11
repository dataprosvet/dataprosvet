Created: 2022-11-01 15:11:91
Tags: #ML #DataScience #confusion_matrix #classification_metric 

## Note
 
 In the field of [[machine learning]], *confusion matrix* also know as an error matrix, is a specific table layout that allows visualization of performance machine
 learning algorithm.

Each row of the matrix represents true class label while each column represents predicted class label.

Confusion matrix visualization:
![](https://miro.medium.com/max/1218/1*jMs1RmSwnYgR9CsBw-z1dw.png)

### TP (True positive)
Sample where model classified it as positive and it is actually positive.
### FP (False positive)
Sample where model classified it as positive but it is negative (***Type 1 error***)
### TN (True negative)
Sample where model classified it as negative and it is actually negative.
### FN (False negative)
Sample where model classified it as negative but it is positive (***Type 2 error***)

>[!NOTE]
>We should always minimize FP and FN rate, but in real cases it is important to minimize only one of these metrics.

Now we can use TP, FP, TN and FN definitions to define classification metrics such as [[Wiki/ml/metrics/Accuracy score|Accuracy score]], [[Wiki/ml/metrics/Precision|Precision]] and [[Wiki/ml/metrics/Recall|Recall]].

### [[TPR (True Positive Rate)]]
Also know as sensitivity (or [[Wiki/ml/metrics/Recall|Recall]]) defines as:
$$TPR=\frac{TP}{TP + FN}$$

### [[FPR (False Positive Rate)]]
Also known as fall-out ration defines as:
$$FPR = \frac{FP}{FP + TN}$$
>[!INFO]
>We can use TRP and FPR to define [[Wiki/ml/metrics/ROC Curve & ROC AUC|ROC Curve & ROC AUC]]

## References
- [Confusion matrix explanation](https://en.m.wikipedia.org/wiki/Confusion_matrix)
- [TRP](https://en.wikipedia.org/wiki/Sensitivity_and_specificity)
- [FPR](https://en.wikipedia.org/wiki/False_positive_rate)

## Zero Links
- [[Wiki/ml/metrics/Classification Metrics|Classification Metrics]]
# performance-metrics-from-scratch
This repository has the implementation of Performance Metrics (e.g. F1 score, AUC, Accuracy, etc) from scratch, without using Scikit Learn library.
<h1>Datasets used in this project</h1>

![image](https://user-images.githubusercontent.com/86348193/215730834-522da7ca-5117-41d1-883b-f7286bb6fcdc.png)
1. <b>sample1.csv :</b> In this dataset, the data is highly imbalanced (number of positive data points >> number of negative data points). The dataset has 2 columns namely 'y' and 'proba' which are basically the actual label of the data point and the probability score of the data point respectively.
2. <b>sample2.csv:</b> In this dataset, the data is highly imbalanced (number of positive data points << number of negative data points). The dataset has 2 columns namely 'y' and 'proba' which are basically the actual label of the data point and the probability score of the data point respectively.
3. <b>sample3.csv :</b> This is a regression data which means the labels are continuous numbers (97, 101.23, etc.). This dataset is used to calculate metrics like MSE, MAPE, R Sqaured error. 
<h1>Performance Metrics Explored</h1>
<h3>1. Confusion Matrix -</h3>

![image](https://user-images.githubusercontent.com/86348193/215733307-636800d9-feb6-476f-a8a9-ffb413715536.png) <br>
Confusion Matrix is the combination of TP, FP, TN, FN in which TP is True Positive, FP is False Positive, TN is True Negative, FN is False Negative.<br>
True Positive - The classifier predicted the label as Positive which is actually Positive.<br>
False Positive - The classifier predicted the label as Positive but actually the label is Negative.<br>
True Negative - The classifier predicted the label as Negative which is actually Negative.<br>
False Negative - The classifier predicted the label as Negative but actually the label is Positive.<br>
<h3>2. F1 Score -</h3>

![image](https://user-images.githubusercontent.com/86348193/215751474-eb6c3e5f-e925-4e68-b1db-c411d332023f.png) <br>
F1 score is the harmonic mean of precision and recall. Harmonic mean for a and b is 2ab/(a+b).<br>
Precision - Out of all the predicted positive data points, how much positive data points was classifier able to predict correctly.<br>
Precision = TP/(TP+FP).<br>
Recall - Out of all the actual positive data points, how much positive data points was classifier able to predict correctly.<br>
Recall = TP/(TP+FN).<br>
<h3>3. Accuracy -</h3>

![image](https://user-images.githubusercontent.com/86348193/215756006-038703d1-4047-459a-8ba0-741b3b6d3ab6.png) <br>
Accuracy is the metric in which out of total predictions, how much the classifier is able to predict correctly, both for positive and negative predictions.<br>
Accuracy = (TP+TN)/(TP+FP+TN+FN).<br>
<h3>4. AUC Score -</h3>

![image](https://user-images.githubusercontent.com/86348193/215759463-0f567dde-ccc9-4887-9cfd-807ef557bf2b.png) <br>
AUC (Area Under Curve) is a performance measurement metric for classification problems at various threshold settings. FPR and TPR are used to calculate AUC Score.<br>
False Positive Rate (FPR) - Out of all the negative data points, how many data points was classifier able to pick up. It is also called as negative recall.<br>
FPR = FP/(FP+TN).<br>
True Positive Rate (TPR) - Out of all the positive data points, how many data points was classifier able to pick up. It is also called as positive recall.<br>
TPR = TP/(TP+FN).<br>
<h3>5. Mean Squared Error (MSE) -</h3>

![image](https://user-images.githubusercontent.com/86348193/215762395-3e1bb3f3-4037-48f1-9a8d-b96688fed90f.png) <br>
MSE is a metric to measure the average of the squares of the errors. This metric is used for regression problems where data is continuous in nature. So the output of this metric does not lie in between some intervals like 0 and 1.<br>
<h3>6. Mean Absolute Percentage Error (MAPE) -</h3>

![image](https://user-images.githubusercontent.com/86348193/215767935-442e4147-66db-44d4-911c-0725de2d5fbf.png) <br>
MAPE is a metric to measure the average of the absolute percentage errors. This metric is used for regression problems where data is continuous in nature.<br>
<h3>7. R Squared Error -</h3>

![image](https://user-images.githubusercontent.com/86348193/215768846-4690776f-bb57-460c-97b1-209e6a12897f.png) <br>
R Squared Error is the comparison of residual sum of squares (SSres) with the total sum of sqaures (SStotal). It represents the goodness of fit of a regression model.<br>
SSres - It is the sum of squares of the residual error which is nothing but the Mean Squared Error (MSE).<br>
SStotal - It is the sum of the squares of the total error which is the sum of the squares of the differences between the actual labels and the mean of the actual labels, which is nothing but the variance value.<br>

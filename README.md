# Credit-Card-Fraud-Detection
Identification of fraudulent credit card transactions - anomaly detection

### Introduction
It is important for credit card companies to able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.

### Dataset
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud <br>

The dataset contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions. <br>

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise. <br>

### Model

1. Isolation Forest Algorithm: <br>
This model excels at identifying anomalies by isolating data points based on their uniqueness, making it highly efficient and effective. Unlike traditional methods, Isolation Forests have low time complexity and memory requirements, building robust models with minimal computational resources. <br> 
Isolation Forests work by randomly selecting features and split values to isolate anomalies with minimal conditions, while normal observations require more conditions for separation. An anomaly score is calculated based on the number of conditions needed to isolate an observation in the constructed isolation trees. <br> <br>

2. Local Outlier Factor (LOF) Algorithm <br> 
LOF is an unsupervised outlier detection method that evaluates the local density deviation of a data point compared to its neighbors. It identifies outliers as samples with significantly lower density than their neighboring points. <br>
The parameter n_neighbors determines the number of neighbors considered. It is typically chosen to be greater than the minimum number of objects a cluster must contain and smaller than the maximum number of nearby objects that could potentially be outliers. In practice, setting n_neighbors to 20 is often effective when such information is not available.

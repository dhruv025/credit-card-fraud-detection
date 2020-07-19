# credit-card-fraud-detection

## In this project, our challenge is to recognize fraudulent credit card transactions so that the customers of credit card companies are not charged for items that they did not purchase. In this, two unsupervised ML algorithms Isolation Forest and Local Outlier Factor(LOF) are used for fraud detection.

## Major Steps followed during the project:

### 1.Data Gathering:

Dataset has been downloaded from kaggle. The dataset consist of 284807 rows and 31 columns. In this dataset, the class column has two values 0 and 1 in which 0 indicates that particular case is not fraud and 1 indicate that particular case is fraud.

### 2.Feature Engineering:

In this, first of all I have checked for the missing values in the dataset if any. In this, dataset there are no missing values.

Also, done exploratory data analysis to analyze the data with the help of seaborn library which is used for data visualization from which I came to know that the count of no. of fraud cases (492) is very less as compared to non-fraud cases (284315).
So, we can conclude that the given dataset is imbalanced.

Since, the dataset contains only numerical values, so is in this dataset we don’t have to handle categorical features.

Now, our dataset is ready for applying to any machine learning algorithm.

### 3.Model Training:

In this first of all, I have divided the dataset into train and test using the train_test_split method of sklearn library.

For training the dataset, I have used two classification algorithms Isolation Forest and Local Outlier Factor. Although, the dataset is imbalanced, but we need not to handle the imbalanced dataset as these two classification algorithm will take care of the imbalanced dataset.

Since, only accuracy doesn’t tells that how good our model is. So, we have to calculate other performance metrics such as precision, recall, support. These performance metrics can be calculated with the help of classification report.
A classification report is used to measure the quality of predictions from a classification algorithm.

### Observation:

1.Isolation Forest detected 683 errors whereas Local Outlier Factor detected 935 errors.

2.Isolation Forest has a accuracy of 99.76% more accurate than LOF of 99.67%.

3.When comparing precision and recall for both the models, the Isolation Forest algorithm perform much better than LOF.

4.So, overall Isolation Forest algorithm performed much better in determining the fraud cases.

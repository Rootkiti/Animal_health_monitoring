# Animal_health_monitoring
This machine learning model utilizes symptom inputs to accurately diagnose diseases in Animal. This cutting-edge technology will contributing to the advancement of Animal health monitoring.

## Overview

In this repo, I will be using data obtained from kaggel.
The dataset contains information about 4 unique animals but, I will be more focused on `Cow`.
I will be exploring many classification algorithms using this dataset and each algorithm will have its unique file and later in this journey I will commbine all algorithms in one file and select the one that will score the highest.

### Algorithms that i will use

1. Decision Tree
2. Logistic Regression
3. Random Forest
4. K-Nearest Neighbors
5. Naive Bayes
6. Gradient Boosting Machines


#### 1. Decision Tree

Result & Approach for Algrithm 1 Decision Tree

Approach

1. Data Preparation 
 I imported the dataset and did some exploration. luckily, there was no cleaning stuff the data was already clean. 

2. split
the next step was to split my data into feature matrix X and target vector y. Then I split X and Y into train and test and finally, I split X_tain and y_train into validation data to be used for model validation

3. model build
During model building, I started by Building a baseline prediction. My baseline prediction was a target with the most counts and it scored 0.22

Next, I built my actual model and scored 
on training data: 0.95 <br>
on testing data: 0.79 <br>
on validation data: 0.78 <br>

From here, I decided to do some exploration on my model to see if those are the best scores my model can provide.
my model had a depth of 24 (default) and I decided to find out if there was any other depth that could provide the best score. so, I used a range from 1 to 50 step by 2, and at each step, I had to initialize my model with a new depth value and keep tracking each score on training, testing, and validation data and plotting them to better understand what was going on.

After the plot, I found out that the depth that could give me the best score was 13, and from there I came to the final model which scored 0.79 which I can say is better than 0.78

#### 2. Logistic Regression

Approach and everthing are the same the different here in tha algorithm used `LinearRegressor`

Second Algorithm Is LogisticRegressor and its results are

on training data: 0.83 <br>
on testing data: 0.82 <br>
on validation data: 0.82 <br>

Both Algorithms use the same data but their performance are different.

DecisionTree performed well on training data but looking at testing and validation accuracies, LogisticRegressor is scoring higher.

#### 3. Random Forest classifier

RandomForestClassifier Results with defaoult parametors

on training data: 0.94 <br>
on testing data: 0.77 <br>

I tried This model on different values for `n_estimators`, `max_depth`, and `min_samples_split` and rusults are:

on training data: 0.86 <br>
on testing data: 0.82 <br>






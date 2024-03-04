![icon](https://i.ibb.co/HgZXm3M/animask.png)


# Introduction
Animask framework is a open source software for Anomaly detection using Artificial Intelligence and Deep Learning.

## Table of content
| S. No. | Phase |
|-----:|---------------|
|     1|The Problem|
|     2|Data Collection|
|     3|Data formatting|
|  4   |ML Algorithm selection|
|     5|Training|
|     6|Deployment|

## Features
| S. No. | Features |
|-----:|---------------|
|     1|Auto track dataset|
|     2|Advanced Data analysis|
|     3|Classify anomaly|
|  4   |Anomaly declaration|

# Documetation
## The Problem
Determine what constitutes an anomaly in your dataset. An anomaly is typically a data point that deviates significantly from the expected pattern or behavior.

## Data Collection
Gather a dataset containing both normal and anomalous data points. Ensure that your dataset is representative of the real-world scenarios you want your model to detect anomalies in.

## Data formatting
Extract relevant features from your dataset that can help the model distinguish between normal and anomalous data points. This step may require domain knowledge and experimentation.

## ML Algorithm selection
Choose an appropriate machine learning model for anomaly detection. We will use "Isolation Forest".

`clf = IsolationForest(contamination=0.1)`
`clf.fit(X_train)`
`y_pred = clf.predict(X_test)`

## Training
Isolation Forest model training to the given Dataset.

## Deployment
Once satisfied with the model's performance, deploy it into a production environment where it can automatically detect anomalies in new data.



## Conclusion
1. **Understanding Anomalies:**
   Anomalies are data points that significantly differ from expected patterns or behaviors.

3. **Approach:**
  Define Normal Behavior: Identify typical ranges, trends, or patterns in the data.
  Choose Detection Technique: Select suitable methods like statistical analysis, machine learning, or rule-based systems.
  Preprocess Data: Clean, normalize, and transform data for analysis.
  Apply Detection Algorithm: Utilize chosen techniques to identify anomalies.
  Evaluate Performance: Assess the accuracy of anomaly detection using appropriate metrics.

3. **Interpretation and Validation:**
  Investigate detected anomalies to understand causes and implications.
  Validate anomalies to ensure they're genuine and not due to errors.

5. **Continuous Improvement:**
  Anomaly detection is iterative; refine techniques based on feedback and validation.

6. **Benefits:**
  Early identification of unusual data points.
  Enhances decision-making and risk management.
  Improves data quality and integrity.


## More on the algorithm.
Isolation Forest is an unsupervised machine learning algorithm used for anomaly detection. It works by isolating anomalies in the dataset rather than profiling normal data points. This algorithm is particularly efficient for detecting anomalies in high-dimensional datasets.

**Here's how the Isolation Forest algorithm works:**

**Random selection of features and splitting:** It selects a random feature and then a random split value between the maximum and minimum values of the selected feature.

**Partitioning data:** The data is then partitioned based on the randomly selected feature and split value. Data points falling on one side of the split are grouped together, while the others fall on the other side.

**Recursive partitioning:** This process of selecting random features and splitting continues recursively until all data points are isolated into individual trees or until a predefined maximum tree depth is reached.

**Anomaly scoring:** Anomalies are expected to be easier to isolate than normal data points. Therefore, if a data point requires fewer partitions to be isolated, it is likely to be an anomaly. The isolation score for each data point is calculated based on the average path length in the trees.

**Thresholding:** The anomaly score is compared to a threshold value. Data points with scores higher than this threshold are considered anomalies.

By isolating anomalies efficiently, Isolation Forest can detect outliers in the dataset without needing to define what constitutes normal behavior explicitly. It's particularly useful for datasets with high dimensionality and large amounts of data. Additionally, it's relatively insensitive to the size of the dataset and can handle both numerical and categorical data.





# Introduction
Anomalisk framework is a open source software for Anomaly detection using Artificial Intelligence and Deep Learning.

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






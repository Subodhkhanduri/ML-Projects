# ML-Projects
This repository contains a collection of machine learning projects and Jupyter notebooks. Each project explores a specific machine learning technique and its application to a real-world dataset.

Project 1: Dimensionality Reduction using Clustering

This project demonstrates the use of K-Means clustering for dimensionality reduction. The goal is to improve the efficiency of a classification model while maintaining or improving its accuracy.

Methodology:

1. Dataset: Human Activity Recognition Using Smartphones (HAR) dataset from the UCI Machine Learning Repository.

2. Preprocessing: The raw data, with 561 features, is first scaled using StandardScaler.

3. Baseline Model: A GaussianNB (Naive Bayes) classifier is trained on the full 561 features to establish a performance benchmark.

3. Dimensionality Reduction: K-Means clustering is applied to the features (by transposing the data) to group similar features together. A representative feature from each cluster is selected to form a reduced feature set. In this case, the number of clusters was set to 50, effectively reducing the feature count from 561 to 50.

4. Reduced Model: The GaussianNB classifier is then trained on the reduced feature set.

5. Results:
The model trained on the reduced feature set achieved a higher accuracy (78.59%) and a significantly faster training time (0.012 seconds) compared to the baseline model's accuracy of 73.15% and training time of 0.15 seconds. This demonstrates that clustering-based dimensionality reduction can be a highly effective technique for improving model performance and efficiency.

Project 2: Clustering Customer Invoice Data

This notebook explores customer segmentation using clustering algorithms on a transactional dataset. The objective is to group customers into distinct segments based on their purchasing behavior.

Methodology:

1. Dataset: Online Retail dataset from the UCI Machine Learning Repository.

2. Preprocessing: The data is cleaned and aggregated at the customer level to create features such as Total_Bill_Size and Purchase_Interval_Days.

3. Clustering:

K-Means: The notebook first applies K-Means clustering to segment customers based on their Total_Bill_Size, identifying different spending groups.

DBSCAN: It then uses DBSCAN, a density-based clustering algorithm, on the normalized Total_Bill_Size and Purchase_Interval_Days to identify clusters of varying shapes and sizes, and to detect outliers (noise points).

Key Findings:

• K-Means: Identified three distinct customer segments based on their total spending, with one cluster representing a small number of very high-value customers.

• DBSCAN: Confirmed the presence of a large, dense cluster of regular customers and identified a smaller number of high-value customers and outliers, validating the initial K-Means findings and providing a more nuanced view of the customer data.

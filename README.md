 Obesity Level Estimation Based on Eating Habits and Physical Condition
Project Overview
This project focuses on a comprehensive data analysis to estimate obesity levels using the "Estimation of Obesity Levels Based On Eating Habits and Physical Condition" dataset. This dataset comprises information on 2,111 individuals, detailing characteristics related to eating habits, physical activity, and other lifestyle factors. The core objective was to apply and understand various machine learning techniques, from data preparation to model deployment, specifically for predicting an individual's obesity level and Body Mass Index (BMI).

Key Features & Methodologies
The project involved several stages of data science workflow:

Data Preprocessing & Feature Engineering:

Thorough data cleaning was performed, including handling duplicates and outliers (e.g., removal of 24 duplicate entries and 303 outliers using the IQR method).

Min-Max Scaling was applied to continuous features (like age, height, weight) to normalize the data, which is crucial for neural network performance.

A mixed approach to feature encoding was used for categorical variables, including Label Encoding for binary features, Ordinal Encoding for features with a natural order, and One-Hot Encoding for nominal categories.

Clustering Analysis:

Explored patterns within the dataset, particularly focusing on dietary habits, using two popular clustering algorithms:

K-means: Identified 12 clusters with an optimal k value determined by the Elbow Method, achieving a Silhouette Score of 0.6230.

DBSCAN: Demonstrated superior adaptability by automatically identifying 15 density-based clusters, with optimized parameters (eps=0.5, min_samples=6) and a higher Silhouette Score of 0.652.

Obesity Category Classification:

Built and evaluated models to predict discrete obesity categories (NObeyesdad).

Random Forest: Achieved an accuracy of 95.71% after hyperparameter tuning.

Multi-Layer Perceptron (MLP) Neural Network: Showcased slightly better performance with an accuracy of 96.86%, along with strong precision, recall, F1-scores, and near-perfect AUC-ROC curves.

BMI Value Regression:

Developed models to predict continuous BMI values.

Feedforward Neural Network: Provided a solid baseline for BMI prediction.

Transfer Learning (Autoencoder-based): This advanced approach leveraged an Autoencoder for unsupervised feature extraction, significantly improving prediction accuracy (demonstrated by better MAE and MAPE scores) compared to the simple Feedforward Network.

Technologies Used
Python

Scikit-Learn

TensorFlow/Keras

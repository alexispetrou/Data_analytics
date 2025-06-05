# Obesity Level Estimation Based on Eating Habits and Physical Condition

## Project Overview  
This project provides a comprehensive data analysis to estimate obesity levels using the "Estimation of Obesity Levels Based On Eating Habits and Physical Condition" dataset. This dataset contains information on 2,111 individuals, focusing on characteristics related to eating habits, physical activity, and other lifestyle factors. The primary goal was to apply and understand various machine learning techniques—from data preparation to model deployment—for predicting an individual's obesity level and Body Mass Index (BMI).

## Key Features & Methodologies  
The project involved several critical stages of the data science workflow:

### Data Preprocessing & Feature Engineering  
- **Data Cleaning**: Performed thorough cleaning, including the removal of 24 duplicate entries and 303 outliers (14.5% of the dataset) using the IQR method.  
- **Normalization**: Applied Min-Max Scaling to continuous features (e.g., age, height, weight) to normalize the data, which is essential for neural network performance.  
- **Feature Encoding**: Utilized a mixed approach for categorical variables:  
  - Label Encoding for binary features.  
  - Ordinal Encoding for features with a natural order.  
  - One-Hot Encoding for nominal categories.  

### Clustering Analysis  
Explored patterns within the dataset, particularly focusing on dietary habits, using two popular clustering algorithms:  
- **K-means**: Identified 12 clusters (optimal k via Elbow Method), achieving a Silhouette Score of 0.6230.  
- **DBSCAN**: Demonstrated superior adaptability by automatically identifying 15 density-based clusters, with optimized parameters (eps=0.5, min_samples=6) and a higher Silhouette Score of 0.652.  

### Obesity Category Classification  
Built and evaluated models to predict discrete obesity categories (NObeyesdad):  
- **Random Forest**: Achieved an accuracy of 95.71% after hyperparameter tuning.  
- **Multi-Layer Perceptron (MLP) Neural Network**: Slightly outperformed Random Forest with an accuracy of 96.86%, showcasing stronger performance across precision, recall, F1-scores, and near-perfect AUC-ROC curves.  

### BMI Value Regression  
Developed models to predict continuous Body Mass Index (BMI) values:  
- **Feedforward Neural Network**: Provided a solid baseline for BMI prediction.  
- **Transfer Learning (Autoencoder-based)**: This advanced approach leveraged an Autoencoder for unsupervised feature extraction, significantly improving prediction accuracy (demonstrated by better MAE and MAPE scores) compared to the simple Feedforward Network.  

## Technologies Used  
- Python  
- Scikit-Learn  
- TensorFlow/Keras  

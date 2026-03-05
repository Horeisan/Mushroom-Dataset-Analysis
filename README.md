# Mushroom-Dataset-Analysis
A supervised learning project focused on classifying mushrooms as edible or poisonous using model evaluation techniques.

This project is a practical application of model evaluation and optimization techniques using the Mushroom Dataset. The main goal was to build a classifier that can 
distinguish between edible and poisonous mushrooms while focusing on rigorous validation.

## 1. Data Processing and Encoding
One-Hot Encoding: Since all features in the dataset are categorical, I applied One-Hot Encoding to convert them into a numerical format.

Pipelines: I used Pipeline objects to chain the preprocessing steps with the models. This ensured that the encoding was applied correctly during both training and cross-validation, preventing any data leakage.

## 2. Supervised Models and Tuning
I experimented with several classification models to compare their performance:

Logistic Regression and SVM: Used as baseline classifiers to understand linear separability.
Random Forest: I implemented a Random Forest model to better capture the non-linear patterns in the mushroom features and improve generalization on the test set.

Grid Search and Randomized Search: I used GridSearchCV and RandomizedSearchCV to tune hyperparameters (like regularization strengths and tree depth). My goal was to find the most stable configuration that generalizes well to unseen data.

## 3. Advanced Evaluation
Confusion Matrix: I generated heatmaps to visualize the distribution of errors, focusing specifically on eliminating (False Edibles).

K-Fold Cross-Validation: I calculated the mean and standard deviation of scores across 5/10 folds to verify the model's stability.

ROC/AUC Analysis: I plotted the ROC curves to measure the diagnostic ability of the classifiers. I noticed some interesting behavior where the model performed better when class labels were effectively analyzed against the decision threshold.

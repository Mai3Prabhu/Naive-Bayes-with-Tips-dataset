# Tips Dataset Time Prediction using Gaussian Naive Bayes

This project demonstrates how to predict the time (Dinner or Lunch) of a customer's visit using the popular "tips" dataset from Seaborn. We employ a Gaussian Naive Bayes classifier, a probabilistic machine learning algorithm well-suited for continuous features.

## Project Overview

The core objective is to build a classification model that can accurately determine if a dining experience was during "Dinner" or "Lunch" based on other features in the dataset. The project follows these key steps:

1. Data Loading: Loading the "tips" dataset.

2. Data Preparation: Separating features (X) from the target variable (y).

3. Categorical Feature Encoding: Converting categorical variables into a numerical format suitable for machine learning models using one-hot encoding.

4. Data Splitting: Dividing the dataset into training and testing sets.

5. Model Training: Training a Gaussian Naive Bayes model.

6. Prediction: Making predictions on unseen test data.

7. Model Evaluation: Assessing the model's performance using standard metrics.

## Dataset

The "tips" dataset, available through the seaborn library, contains information about the tips received by a waiter over a period of time. Key columns relevant to this project include:

- total_bill: Total bill amount (continuous)
- tip: Tip amount (continuous)
- sex: Gender of the payer (categorical)
- smoker: Whether the party included smokers (categorical)
- day: Day of the week (categorical)
- time: Time of day (Dinner or Lunch) - This is our target variable
- size: Size of the party (numerical)

## Key Libraries Used

1. seaborn: For loading the "tips" dataset.

2. pandas: For data manipulation, especially for one-hot encoding.

3. scikit-learn: For data splitting, the Gaussian Naive Bayes model, and evaluation metrics.

## Results

The Gaussian Naive Bayes model demonstrated strong performance in predicting the time of the customer's visit.

Accuracy:
```
0.9591836734693877
```

Confusion Matrix:
```
[[32  2]
 [ 0 15]]
```

This matrix indicates:

- 32 instances of "Dinner" were correctly predicted as "Dinner".
- 2 instances of "Dinner" were incorrectly predicted as "Lunch".
- 15 instances of "Lunch" were correctly predicted as "Lunch".
- 0 instances of "Lunch" were incorrectly predicted as "Dinner".

Classification Report:

```
              precision    recall  f1-score   support

      Dinner       1.00      0.94      0.97        34
       Lunch       0.88      1.00      0.94        15

    accuracy                           0.96        49
   macro avg       0.94      0.97      0.95        49
weighted avg       0.96      0.96      0.96        49
```

The model achieved an impressive 96% accuracy on the test data. It showed perfect recall for "Lunch" predictions and high precision for "Dinner" predictions.

## Conclusion

The Gaussian Naive Bayes model proved to be highly effective in classifying the time of day (Dinner/Lunch) from the "tips" dataset, achieving a high accuracy of 96%. This highlights its suitability for multiclass classification problems with a mix of continuous and categorical features (after appropriate encoding).

## How to Run

**1. Clone the repository:**

```
git clone https://github.com/your-username/your-repo-name.git # Replace with your actual repo URL
cd your-project-folder # Navigate to your project directory
```

**2. Install dependencies:**

Ensure you have the necessary libraries installed:
```
pip install seaborn pandas scikit-learn numpy
```

**3. Run the script:**

Save the provided code into a Python file (e.g., tips_prediction.py) and run it from your terminal:
```
python tips_prediction.py
```

## Contributing
Contributions, issues, and feature requests are welcome! Feel free to fork the repository and submit pull requests.

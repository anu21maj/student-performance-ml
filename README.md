# Student Performance Prediction Using Machine Learning

## Project Overview

This project explores the use of machine learning to predict whether
a student passes or fails based on selected demographic and academic
characteristics.

The project uses Python and classical machine learning algorithms to
explore the dataset, preprocess features, train classification models,
and compare their performance.

## Objectives

- Explore and understand student performance data.
- Perform exploratory data analysis (EDA).
- Prepare numerical and categorical features for machine learning.
- Train and evaluate classification models.
- Compare models using accuracy, precision, recall, and F1-score.
- Understand the limitations of predictive models.

## Dataset

The project uses the Student Performance dataset from the UCI Machine
Learning Repository.

The mathematics dataset contains 395 student records and 33 original
attributes.

The target variable is created from the final mathematics grade, G3:

- Pass (1): G3 >= 10
- Fail (0): G3 < 10

The model uses the following features:

- Age
- Study time
- Previous failures
- Absences
- Mother's education
- Father's education

The previous period grades, G1 and G2, are excluded from the selected
features so the models do not rely directly on those earlier grades.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning Workflow

1. Load and inspect the dataset.
2. Explore the distribution of student outcomes.
3. Visualize relationships between selected features and outcomes.
4. Create a binary pass/fail target variable.
5. Select features and split the data into training and test sets.
6. Preprocess numerical and categorical features.
7. Train Logistic Regression and Gaussian Naive Bayes models.
8. Evaluate and compare model performance.

## Results

The following results were obtained on the selected test set:

| Metric | Logistic Regression | Gaussian Naive Bayes |
|---|---:|---:|
| Accuracy | 69.6% | 51.9% |
| Fail Precision | 56.2% | 38.9% |
| Fail Recall | 34.6% | 80.8% |
| Fail F1-score | 42.9% | 52.5% |

Logistic Regression achieved higher overall accuracy, while Gaussian
Naive Bayes achieved higher recall and F1-score for the Fail class.

This comparison demonstrates why accuracy should not be used as the
only evaluation metric.

## Limitations

- The dataset is relatively small and represents mathematics
  performance at two Portuguese schools.
- The models use only a subset of the available features.
- The results depend on the selected train-test split.
- Predictive associations do not establish causation.
- The models have not been validated for real-world educational use.

## Future Improvements

- Apply cross-validation for more reliable evaluation.
- Explore additional features.
- Tune model hyperparameters.
- Experiment with additional classification algorithms.
- Investigate methods for improving identification of students
  at risk of failing.

## Project Structure

```text
student-performance-ml/
├── data/
│   └── student-mat.csv
├── notebooks/
│   └── student_performance.ipynb
├── requirements.txt
└── README.md
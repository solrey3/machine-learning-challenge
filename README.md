# Machine Learning Homework - Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)

### Before You Begin

1. Create a new repository for this project called `machine-learning-challenge`. **Do not add this homework to an existing repository**.

2. Clone the new repository to your computer.

3. Give each model you choose their own Jupyter notebook, **do not use more than one model per notebook.**

4. Save your best model to a file. This will be the model used to test your accuracy and used for grading.

5. Commit your Jupyter notebooks and model file and push them to GitHub.

## Note

Keep in mind that this homework is optional! However, you will gain a much greater understanding of testing and tuning different Classification models if you do complete it.

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.

In this homework assignment, you will need to:

1. [Preprocess the raw data](#Preprocessing)
2. [Tune the models](#Tune-Model-Parameters)
3. [Compare two or more models](#Evaluate-Model-Performance)

- - -

## Instructions

### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

### Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

### Reporting

* Create a README that reports a comparison of each model's performance as well as a summary about your findings and any assumptions you can make based on your model (is your model good enough to predict new exoplanets? Why or why not? What would make your model be better at predicting new exoplanets?).

## Summary About Findings

* Random Forest, KNN, and SVM are very conclusive in regards to identifying false positives.
* Hyperparameter tuning showed improvements in Training Grid Scores and Testing Grid Scores.
* Random Forest model appears to provide most accurate results even when compared to Neural Network and Deep Learning models.

### Random Forest
Random Forest model is very conclusive in regards to identifying false positives (f1-score, FALSE POSITIVE = 0.99).

Hyperparameter tuning changed Testing Grid Score from 0.8907322654462243 to 0.8947368421052632

### KNN
KNN is very conclusive in regards to identifying false positives (f1-score, FALSE POSITIVE = 0.99).

Hyperparameter tuning changed Training Grid Score from 0.8258630555025749 to 1.0

Hyperparameter tuning changed Testing Grid Score from 0.8094965675057209 to 0.8335240274599542.

Best Grid Results are with n = 17:
* {'metric': 'manhattan', 'n_neighbors': 17, 'weights': 'distance'}
* 0.8491290439840059
* KNeighborsClassifier(metric='manhattan', n_neighbors=17, weights='distance')

### SVM
SVM is very conclusive in regards to identifying false positives (f1-score, FALSE POSITIVE = 0.99).

Hyperparameter tuning changed Training Grid Score from 0.8498950982262063 to 0.8775510204081632.

Hyperparameter tuning changed Testing Grid Score from 0.8329519450800915 to 0.8655606407322655.

Best Grid Results are with c = 10 as opposed to 1 or 5.
- {'C': 10, 'gamma': 0.0001}
- 0.8733555767397521

### Neural Network and Deep Learning
Neural Network Accuracy: 0.8598397970199585

Deep Learning Accuracy: 0.8890160322189331

- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -



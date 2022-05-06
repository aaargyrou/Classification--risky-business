# Unit 11 - Risky Business
## Background

In this assignment I build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so you I employ different techniques for training and evaluating models with imbalanced classes. 

The imbalanced-learn and Scikit-learn libraries are used to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

- - -

## Files

[Resampling Starter Notebook](Code/credit_risk_resampling.ipynb)

[Ensemble Starter Notebook](Code/credit_risk_ensemble.ipynb)

[Lending Club Loans Data](Resources/LoanStats_2019Q1.csv.zip)

- - -

## Credit Risk Resampling

### Oversampling
Random Oversampling includes selecting random examples from the minority class with replacement and supplementing the training data with multiple copies of this instance, hence it is possible that a single instance may be selected multiple times.

Oversampling techniques used were the following:
* Random oversampler
* SMOTE (Synthetic Minority Oversampling Technique)

### Undersampling
Random Undersampling is the opposite to Random Oversampling. This method seeks to randomly select and remove samples from the majority class, consequently reducing the number of examples in the majority class in the transformed data.

### Combination Sampling
This involces combining the two above methods. Using the SMOTE and Edited Nearest Mean (SMOTEENN) techniques.

### Questions

1. Which model had the best balanced accuracy score?

   The random oversampler and the SNMOTEEN algorithm had the best balanced accuracy score (bas) of 0.9948

2. Which model had the best recall score?

    Both oversampling techniques (random over sampling and SMOTE), the combined sampling method (SMOTEENN) all performed similar with a recall of 0.99

3. Which model had the best geometric mean score?

    Similar to the bas, the random oversampler and SMOTEENN both had geometric mean of 0.9947

- - -
## Ensemble Learning

In this section, you will train and compare two different ensemble classifiers to predict loan risk and evaluate each model. You will use the [Balanced Random Forest Classifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html) and the [Easy Ensemble Classifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html). Refer to the documentation for each of these to read about the models and see examples of the code.

1. Which model had the best balanced accuracy score?

    Easy ensemble classifier had the best balanced accuracy score of 0.91 compared to the Balanced Random Forest Classifier of 0.77

2. Which model had the best recall score?

    Easy ensemble classifier had the best recall score of 0.95 compared to the Balanced Random Forest Classifier of 0.92

3. Which model had the best geometric mean score?

    Easy ensemble classifier had the best geometric mean score of 0.91 compared to the Balanced Random Forest Classifier of 0.75

4. What are the top three features?

    * total_rec_prncp = 0.081423
    * total_pymnt = 0.070869
    * last_pymnt_amnt = 0.070476

- - -
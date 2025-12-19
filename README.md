# Adult Census Classification (MLDM)

This repository contains a machine learning classification project that I completed as part of
the **Machine Learning and Data Mining** module in my MSc Data Science programme at the
**University of Salford**.

In this project, I worked with the UCI Adult Census dataset and applied supervised learning
techniques to explore how demographic and employment-related factors can be used to predict
different work patterns. The focus was not only on model performance, but also on building a
clear, reproducible workflow and reflecting on ethical considerations when working with
demographic data.



## Project Aims

The main aim of this project was to design and implement a complete machine learning pipeline
using a real-world dataset. Specifically, I aimed to:
- Explore and understand the structure of the Adult Census dataset through EDA
- Prepare mixed numerical and categorical data using reusable preprocessing pipelines
- Train and evaluate multiple classification models
- Compare model performance and interpret their results
- Reflect on potential bias and ethical implications of using census data



## Prediction Tasks

Rather than focusing only on income prediction, I reformulated the dataset into two practical
multi-class classification tasks:

1. **Workclass Prediction**  
   Predicting an individual’s employment sector (such as Private, Self-employed, or Government)
   based on demographic and job-related attributes.

2. **Hours-per-week Classification**  
   Grouping individuals into meaningful working-hour categories:
   - Part-time (≤30 hours)
   - Full-time (31–40 hours)
   - Over-time (>40 hours)

These tasks were chosen to demonstrate how the same dataset can be adapted to answer
different analytical questions.



## Dataset

- **Source:** UCI Adult Census Dataset (accessed via OpenML)  
- **Link:** https://www.openml.org/d/1590  
- **Size:** 48,842 records  
- **Features:** Age, education, occupation, workclass, hours-per-week, and other demographic variables

The dataset contains a mix of numerical and categorical features, making it well suited for
testing preprocessing strategies and classification models.



## Methods and Tools

### Models Used
- **Logistic Regression (One-vs-Rest)**  
  Used as a simple and interpretable baseline model.
- **Random Forest Classifier**  
  Used to capture non-linear relationships and feature interactions.

### Libraries
- Python
- pandas and numpy for data handling
- seaborn and matplotlib for visualisation
- scikit-learn for preprocessing, pipelines, modelling, and evaluation



## Workflow Overview

The project follows a structured and reproducible workflow:
1. Loading the dataset from OpenML
2. Performing exploratory data analysis (EDA)
3. Building preprocessing pipelines using `ColumnTransformer`
4. Splitting the data into training and test sets using stratification
5. Training Logistic Regression and Random Forest models
6. Evaluating performance using multiple metrics
7. Interpreting results and reflecting on their implications



## Model Evaluation

To evaluate model performance, I used:
- Accuracy
- Macro-averaged Precision, Recall, and F1-score
- Confusion matrices for detailed error analysis

Macro-averaged metrics were chosen to ensure that less frequent classes were treated fairly,
rather than being dominated by majority classes.



## Ethical Considerations

Although the Adult Census dataset is anonymised and publicly available, it includes sensitive
attributes such as sex, race, and education level. Predictions produced by these models are
probabilistic and should not be used in isolation to make employment-related decisions.
Any real-world use would require fairness checks, transparency, and human oversight.




**Ayomide Ogunmakinwa**  
MSc Data Science  
University of Salford

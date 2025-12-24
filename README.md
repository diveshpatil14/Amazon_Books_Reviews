Amazon Books Popularity Prediction using Machine Learning
Project Overview

This project analyses an English-language Amazon Books dataset to understand what factors influence book popularity and to predict popularity using machine learning techniques. Book popularity is measured using engagement-based metrics derived from user ratings and reviews. The project follows a structured Knowledge Discovery in Databases (KDD) methodology and focuses not only on prediction accuracy but also on model interpretability.

Research Question

Using only book Metadata, can machine learning models, predict	a books, popularity (ratings_count, text_review_count) and which metadata features are the strongest predictors of popularity?

Dataset Description

Source: Kaggle

Dataset: Amazon Books Metadata

Language Filter: Only English-language books (eng, en-US, en-GB)

Final Size: ~10,000+ books after cleaning

Key Features Used

average_rating

ratings_count

text_reviews_count

num_pages

publication_year

books_age 

rating_per_page 

reviews_per_rating 

Target Variable

log_ratings_count
(Log-transformed popularity metric to reduce skewness and handle outliers)

Methodology (KDD)

The project follows the KDD methodology, consisting of:

Data Selection – Selecting relevant Amazon book metadata and filtering English-only books

Data Preprocessing – Handling skewness, removing invalid entries, log transformation

Data Transformation – Feature engineering and train–test split

Data Mining – Applying machine learning models

Interpretation & Evaluation – Performance comparison and explainability using SHAP

 Models Used
1. Linear Regression

Used as a baseline model

Simple and interpretable

Helps understand linear relationships

 Random Forest Regression

Used as the primary model

Captures non-linear patterns

Performs better on real-world, engagement-based data

 Model Evaluation

Models were evaluated using multiple metrics:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

R² Score

Random Forest significantly outperformed Linear Regression, indicating that book popularity follows non-linear patterns.

Model Interpretability

To satisfy interpretability requirements, SHAP (SHapley Additive exPlanations) was applied:

Explains how each feature affects predictions

Revealed that reviews_per_rating is the most influential feature

Showed that engagement matters more than basic metadata like page count

Related Work

Relevant literature was reviewed using Scopus-indexed research papers and academic sources, including:

Amazon book recommendation and rating prediction studies

Machine learning methods for book popularity and engagement analysis

Theoretical foundations from An Introduction to Statistical Learning (ISLR)


Project Deliverables

Cleaned dataset (CSV)

Jupyter Notebook with full analysis and modelling

Final report (IEEE format)

Presentation (PPT)

Google Drive link containing all data, code, and outputs


Tools & Technologies

Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

SHAP

Jupyter Notebook

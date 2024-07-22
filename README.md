# Udacity Data Science Capstone Project - Sparkify
## Project Description
For the Udacity Data Science Nanodegree, I chose to work on Sparkify, a project that involves developing a large-scale data processing pipeline using Apache Spark to analyze user behavior on a fictional music streaming service called Sparkify.

We were tasked with setting up a Spark cluster and employing Spark SQL and DataFrames to perform ETL (Extract, Transform, Load) operations on a massive dataset containing user activity logs. The project entails using advanced data processing techniques such as filtering, aggregating, and joining large datasets to gain insights into user interactions. 

Additionally, I also implemented machine learning models using Spark's MLlib library to predict user churn, identifying which users are likely to stop using the service. 

The objective is to provide a comprehensive analysis and report that details the methodology, findings, and results.

[The blog post can be found here.](https://roberto-bandeiram.medium.com/churn-it-u%CC%B6p%CC%B6-down-how-sparkify-predicts-customer-churn-with-big-data-78729c82931e)

## Problem Statement
In the context of businesses, especially those offering subscription-based services, understanding and addressing churn is crucial because retaining existing customers is often more cost-effective than acquiring new ones. Churn can be driven by various factors such as dissatisfaction with the service, better offers from competitors, or changes in customer needs and preferences. By analyzing user behavior and identifying patterns that precede churn, companies can implement strategies to improve customer satisfaction and retention, ultimately enhancing their long-term profitability and growth.

## Methodology
1. Exploratory Data Analysis
2. Feature Engineering
3. Churn Prediction Model Evaluation
4. Results Evaluation

### Metrics
The chosen optimization metric for the Churn Prediction Models was F1 score.

Churn prediction is a binary classification problem where the cost of false positives (predicting a user will churn when they won’t) and false negatives (predicting a user won’t churn when they will) can have different business implications. The F1 score, being the harmonic mean of precision and recall, provides a single metric that reflects both aspects, ensuring that the model performs well in identifying true churners without excessively predicting non-churners as churners.

### Models
I tried 2 different models:
* Logistic Regression -> offers a clear and interpretable starting point
* Random Forest -> provides a more complex and accurate model capable of uncovering intricate patterns in the data

## Results
Given the features selected from the Feature Engineering exercise, the Logistic Regression model had a better result with an F1 score of 0.71 on the validation set vs 0.64 for the Random Forest.

It's hard to interpret the number alone, but [industry standards](https://serokell.io/blog/a-guide-to-f1-score) historically consider a score of 0.7 or more to be a good result for classification problems such as this one.

### Next Steps
Although the F1 was relatively good for the Logistic Regression Model, there are other steps that we can take to try to advance this result further:

* Consider other variables like:
** days since sign up
** whether was free or paid right before churn
* Try other models like Naive Bayes, Neural Nets and GBT
* Use pipeline and grid search to combine sequential models and search the best parameters

## Installation
* NumPy
* Pandas
* PySpark SQL
* PySpark ML
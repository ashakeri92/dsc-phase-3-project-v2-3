
# SyriaTel Customer Churn Analysis
**Authors:** Armun Shakeri


### Overview

This project analyzes SyriaTel Customer Churn dataset to explore if there are any predictable patterns with cutomer turnover.

### Business Problem and Data

SyriaTel is interested in reducing the amount of money lost due to customer turnover. This project seeks to analyze customer data and identify any patterns that lead to customer churn. 


### Data

For this project we had SyriaTel's customer churn info, "archive/bigml_59c28831336c6604c800002a.csv". This data set contained 3 columns that were useless for analysis, these columns, "state", "area code", and "phone number", were dropped. We then plotted to data to view any noticable patterns. After those patterns were identified we used onehotencoder to change categorical variables,  "international plan" and "voice mail plan" changing "yes" to 1 and "no" to 0. We will did the same with churn column, but rather than using onehotencoder we used .astype() to change the column to integer. 

### Methods 

The final step in data cleaning was splitting the data using test train plit into feature and target dataframes. We will set X as all variables except "churn" and we will set y to "churn". We will also scaled the X variables for modeling.

### Analysis 

For analysis we decided to use 3 models, logistic regression, DecisionTreeClassifier, and XGBClassifier. The steps for modeling went as follows, build a model, model.predict(), print classification report and confusion matrix for model, and finally determining the fit of the model. The 1st linear regression model did not perform as well as we had expected. To fix this we used SMOTE to balance the data, by creating synthetic values to balance our existing data. The 2nd model showed higher scores that made this model adequate to use if chosen. The 2nd model was the DecisionTreeClassifier, this model showed high results on the classification report and promising numbers on the confusion matrix. The final model plotted was the XGBClassifier, this model showed perfect scores on the classification report for the training data and near perfect scores on the test data. 

### Evaluation and Conclusion 

After analyzing and evaluating the data set from Syria Tel we have 3 recommendations:

1) Bring down costs of day charges

2) offer bonuses for minutes used 

2) Focus more on customer service 

For this analysis we will be choosing XGBClassifier as the chosen model. On the classification report it scored perfectly on the training data and had the highest scores in precision, recall, and f1-score. We want to ensure the model runs as accurateltly as possible, meaning we also want the chosen model to have low false positives and true negatives. The XGBClassifier also falls within this category.

This analysis provides an adequate model that is able to generate predictions on whether a SyriaTel customer will churn or not churn. For the final model we chose the XGBClassifier, due to it's high scores on the classification analysis and high amount of true positives on the confusion matrix.

### Visuals

![graph1](./images/1.png)

First logistic regression scores

![graph2](./images/2.png)

Second logistic regression scores

![graph3](./images/3.png)

Decision tree classification report and confusion matrix

![graph4](./images/4.png)

XGBClassifier classification report

![graph5](./images/Heatmap.png)

Heatmap generated from SyriaTel data 

### For More Information

Please review our full analysis in analysis.ipynb or our [presentation](./DS_Project_Presentation.pdf).

For any additional questions, please contact Armun Shakeri ashakeri62@gmail.com 

## Repository Structure

├── archive
├── images
├── analysis.ipynb
├── archive.zip
├── CONTRIBUTING.md
├── LICENSE.pdf
├── README.md 


## Project 2 - Ames Housing Data and Kaggle Challenge

This project was completed for an immersive data science program at General Assemby. The project required developing a machine learning model to predict housing sale prices. I will be using the popular housing dataset from Ames, Iowa. The particular version of that dataset we were given contained over 1,500 entries of homes sold from 2006 to 2010 with about 80 descriptive features involved in assessing home values. I performed a comprehensive exploration of the data to understand the relationships among features to sale price, as well as identified any skewness, outliers, and missing values. Then, after cleaning the data and undergoing feature selection, I created a machine learning model to predict house sale prices. I utilized linear regression as well as lasso and ridge. The model's efficacy will be evaluated using root mean squared error (RMSE), a metric gauging the disparity between predicted and observed values.

## Data Dictionary

Refer to Kaggle.com to find descriptions of each variable in the Ames Dataset here: https://www.kaggle.com/competitions/dsi-910-ames-housing-challenge/data 
Our dependent variable here is 'SalePrice'

The following features were selected for my final model:
* 'Overall Qual'
* 'Overall Cond'
* 'Year Built',
* 'Year Remod/Add'
* 'Mas Vnr Area'
* '1st Flr SF'
* '2nd Flr SF'
* 'Gr Liv Area'
* 'Full Bath'
* 'Half Bath'
* 'Bedroom AbvGr'
* 'TotRms AbvGrd'
* 'Fireplaces'
* 'Garage Cars'
* 'Garage Area',
* 'Wood Deck SF'
* 'Open Porch SF'
* 'SalePrice'

## EDA & Data Cleaning

I embarked on a comprehensive exploration and refinement of the dataset. Employing a range of visualization techniques such as boxplots and scatterplots, I scrutinized the data to unveil insights into its distribution and relationships between variables. Boxplots enabled me to visually identify the spread and central tendency of categorical features, aiding in the detection of outliers. Scatterplots, on the other hand, facilitated the examination of potential correlations between variables, particularly focusing on their influence on the sale price.

Additionally, I implemented filtering mechanisms to identify and handle outliers. Furthermore, I opted to prioritize numeric features over categorical ones. This involved filtering out most categorical features from the analysis, allowing for a more streamlined and focused exploration of the numerical variables' impact on the target variable.

## Model Development

I initially took a rigorous approach to removing outliers, but this proved detrimental to predictive modeling. However, upon refining the process by specifically addressing the biggest outliers influencing square footage, I observed improvements in model performance. I created a linear, lasso and regression models, employing techniques such as regularization to combat overfitting.

Throughout the model creation phase, I experimented with various feature combinations. Interestingly, I found that adding features often led to decreased model performance. Realizing that adding more features didn't enhance model efficacy, I shifted focus towards identifying the most impactful numeric variables. This led to the development of a better model, detailed and analyzed in the "Baseline vs Model" folder.

## Analysis

Below I will detail the model that performed the best. I analyzed the performance of this model by performing a train-test-split and then comparing the r-squared values of the training vs testing data. I also calculated and compared the mean squared errors. The metrics I calculated were as follows;

Training Set Performance:

Linear Regression:
RMSE: 31442.496
R-squared Score: 0.8416

Lasso Regression:
RMSE: 31442.592
R-squared Score: 0.8416

Ridge Regression:
RMSE: 31455.389
R-squared Score: 0.8415


Test Set Performance:

Linear Regression:
RMSE: 34570.464
R-squared Score: 0.8214

Lasso Regression:
RMSE: 34570.323
R-squared Score: 0.8214

Ridge Regression:
RMSE: 34488.087
R-squared Score: 0.8222

## Analysis:

All three models, Linear Regression, Lasso Regression, and Ridge Regression, achieved similar performance in terms of RMSE and R-squared score, indicating they fit the training data well and explained around 84% of the variance in the target variable.

Similarly, all models exhibit similar performance on the test set with slightly higher RMSE values and slightly lower R-squared scores compared to the training set. This suggests that the models generalize reasonably well to unseen data, though there is a slight drop in performance compared to the training set.
Comparison:

There is little difference in performance between Linear Regression, Lasso Regression, and Ridge Regression, with each method yielding comparable results. However, Ridge Regression slightly outperforms the other methods on the test set in terms of RMSE and R-squared score.
Overall, the models provide a reasonable fit to the data, but there may be opportunities for further refinement or exploration of different modeling techniques to potentially improve predictive performance.

## Future Steps 

* Explore advanced modeling techniques such as ensemble methods or neural networks to capture more complex relationships in the data.
* Identifying key cost drivers such as construction materials, labor costs, and regulatory requirements to incorporate into the modeling process.
* Validating the cost estimation models against actual project costs to assess their accuracy and reliability.
* Incorporating time-series analysis techniques or survival analysis methods to model the probability of a property remaining on the market over time.


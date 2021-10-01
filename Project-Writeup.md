# Interpreting Critical Features of Kickstarter Project Profiles 
Evelyn Johnson

## Abstract
The goal of this project was to use a linear regression modeling techniques to infer which characteristics are most important in predicting the amount of funding a startup will receive. This prediction was based on data acquired through web scraping the most recently successfully-funded projects on Kickstarter in the United States.
I created a lasso regression model to remediate any overfitting of my model to predict the    

## Design
This project provides evidence for which features of a project can indicate the amount of funding it will receive. By employing machine learning models,
start-ups will be able to identify the most important features of a profile in order to maximize funding. 

## Data
The dataset contains 1,080 Kickstarter project profiles with their project title and 10 features for each. Two of the features were categorical, location and
project category. A few feature highlights include the total number of backers, monetary goal, presence of a video, and length of funding period. Exploratory
data analysis was conducted before modeling to assess target and feature relationships and collinearity between features. 

## Algorithms

*Feature Engineering*
1. Stripping the Location column to include the state of project origin and then grouping by regions of the U.S., specifically, northeast, southeast, midwest, southwest, and west
2. Grouping subsets of project categories (n=117) into more general categories (n=15)
3. Converting location and category features to binary dummy variables 
4. Addressing the positively-skewed distribution by excluding outliers where funding was greater than $100,000 

*Models*
Linear regression with a varying selection of features and outlier exclusion criteria were used before lasso regularization was settled on to remediate the issue of overfitting. Six features were filtered out completely with this process (Project We Love Tag, Southwest, Crafts, Dance, Film & Video, Theater). The most significant coefficients were Number of Backers, 11,543.39; Monetary Goal, 6,228.41; Technology, 915.93,  Comics, -879.41; and Number of Backers for Highest Pledge, -738.32.

*Model Evaluation and Selection*
The entire dataset of 1,012 was split into train and holdout, using 80% and 20%, respectively. Using a simple linear regression with five-fold cross validation on the training set, I found my model to be overfit. Since there was no multicollinearity between features, I then standardized the dataset and trained a lasso regularization regression model to perform feature selection.

**Final Lasso Regularization Model:** 10 features 
   - R-sqaured: 0.789
   - MAE: 4152.68
   - RMSE: 7874.45

**Holdout** 
   - R-squared: 0.750 
   - MAE: 4910.49
   - RMSE: 9178.03

## Tools
- BeautifulSoup and Selenium for web-scraping
- Numpy and pandas for data manipulation
- Scikit-learn, pandas and statsmodels  for modeling
- Matplotlib and Seaborn for plotting


## Communication
In addition to this report, a presentation has been created to highlight the importance of this project. 

![Lasso_scatter](https://user-images.githubusercontent.com/84474016/135572157-113b0b3b-4e21-4c8b-8a28-968218c7cc32.png)

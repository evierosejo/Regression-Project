# Interpreting Critical Features of Kickstarter Project Profiles 
Evelyn Johnson

## Abstract
The goal of this project was to use a linear regression model to infer which characteristics are most important in predicting the amount of funding a startup 
will receive. This prediction was based on data acquired through web scraping the most recently successfully-funded projects on Kickstarter in the United States.
I created a lasso regression model to remediate any overfitting of my model to predict the    

## Design
This project provides evidence for which features of a project can indicate the amount of funding it will receive. By employing machine learning models,
start-ups will be able to identify the most important features of a profile in order to maximize funding. 

## Data
The dataset contains 1,080 Kickstarter project profiles with their project title and 10 features for each. Two of the features were categorical, location and
project category. I stripped the string to only include the state of project origin and then grouped by regions of the 
U.S., specifically, northeast, southeast, midwest, southwest, and west. Project categories (n=117) were grouped into more general categories (n=15) before the 
creation of dummy variables. A few feature highlights include the total number of backers, monetary goal, presence of a video, and length of funding period. Exploratory
data analysis was conducted before modeling to assess target and feature relationships and collinearity between features. 

## Algorithms

*Feature Engineering*
The distribution was positively-skewed, smoothing out to zero when funding was greater than $1,000,000. To ensure a better fit model, I removed the rows with a 
Funding value greater $1,000,000. 

*Models*
  
Linear regression model, lasso regularizaiton,

*Model Evaluation and Selection*
  

## Tools
- BeautifulSoup and Selenium for web-scraping
- Numpy and Pandas for data manipulation
- Scikit-learn and statsmodels  for modeling
- Matplotlib and Seaborn for plotting


## Communication
In addition to this report, a presentation has been created to highlight the importance of this project. 

![Lasso_scatter](https://user-images.githubusercontent.com/84474016/135572157-113b0b3b-4e21-4c8b-8a28-968218c7cc32.png)

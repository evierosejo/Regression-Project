# Question:

The purpose of this linear regression model is to predict the amount of funding a startup will receive based on prior 
successfully funded projects on Kickstarter. Through the exploration of this model, those looking to start a funding campaign for a product or company will be able to evaluate the relationships between the amount of funding a startup receives with certain factors.



# Data:

The training data will be acquired from Kickstarter's successful projects discover page with profiles in all categories and from all over the world sorted by the campaign's end date. There are 207,434 campaign profiles that fit this criteria. The factors that I will be using as features in the model are:
1. Project Category
2. Location
3. Presence of "Project We Love" tag (True/False)
4. Number of backers 
5. Goal in certain currency
6. Number of rewards
7. Number of backers for lowest pledge amount
8. Number of backers for highest pledge amount
9. Funding Period Length
10. Video present (True/False)

I will obtain this data by webscraping the profiles of each project located on the Discover page. The target of my model is the amount of funding a project will receive in the U.S. dollar amount. 

# Tools:
I will use Beautiful Soup to parse the HTML script and Selenium to naviagate the Discover page. 

# MVP:
A MVP for my project could be a linear regression model for 1,000 profiles scraped from Kickstarter each with data for all of the aforementioned features.

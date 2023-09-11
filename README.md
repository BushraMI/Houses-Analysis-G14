# Group 14 - Phase 2 Project

<!-- ![Real_Estate](https://media.giphy.com/media/e8ik35i8LaO3BqRwY6/giphy.gif) -->
<img src="https://media.giphy.com/media/e8ik35i8LaO3BqRwY6/giphy.gif" width="700px" height="280px" alt="Header" />

## Project Overview
Real estate in the USA is a diverse and dynamic market that varies significantly by region. Some key facts and trends in the US real estate market include:
1. Housing Market: The US housing market saw a significant increase in demand, driven by cheap mortgage rates, remote work habits, and shifting lifestyle tastes as a result of the COVID-19 pandemic. As a result, Home values rose as a result in several locations.
2. Home Prices: Home prices saw significant appreciation in various metropolitan areas, making housing affordability a concern for many potential buyers. Cities like San Francisco, Seattle, and Austin saw substantial price increases.
3. Urban Migration: The pandemic accelerated the trend of people moving away from densely populated urban areas to suburban and rural locations. 
4. Real Estate Technology: The use of technology in real estate, such as virtual property tours, digital mortgage applications, and blockchain-based property records, continued to evolve.

According to Redfin article: <a href="https://www.redfin.com/us-housing-market" target="blank">United States Housing Market </a>, we are able to see an overview of the United States Housing Market, Demand, Supply.

For this project,we are given the King County House Sales as our base dataset.We are required to use multiple linear regression modeling to analyze house sales in a northwestern county. 

We will be required to Import/Load, Clean, Visualize and Model the data provided. This will enable us to answer the objectives set and provide Recommendations and insights to our audience stakeholders.

## Business Understanding
<img src="image1.jpeg" align="left" width="350px" height="220px" alt="Idea" />

### Stakeholder Audience
Fanaka Group, a Real Estate Investment Group is the identified stakeholders for this project. This group deals with buying, selling, renovating and financing properties.
The group is seeking for ways it can provide better housing facilities for their clients. They are seeking to improve their efficiency and effectiveness in delivering their facilities to their clients.

They have asked us to provide insights and recommendations into the real estate market in terms of which houses and renovation features are likely to give them a significant profit on their investment. 


### Business Objectives
The aim of this project is to analyze the provided dataset on King Country and eventually answer to the Stakeholders questions.
With this in mind, the objectives of this project include:
1. To model and understand the relationship between house sales prices and multiple independent variables(ie the house features).
2. Valuation of the property: 
Identify the key factors that affect house prices in the northwestern county.
3. Customer satisfaction: 
Identify the key factors (features of attraction) affect house sales
4. Provide insights and recommendations to the stakeholders in regards to their investing

## Data Understanding
For this project, we will use the King County House Sales dataset under the file path `data\...` This folder contains historical data of house sales captured in a northwestern country, which we will modify for the purpose of our analysis.

<img src="image2.png" align="left" width="150px" height="100px" alt="Method" />

The data folder includes the following files:
1. `column_names.md` - provides a description of the column names
2. `kc_house_data.csv` - provides list of attributes for the houses and their prices


### Visualization

<div class='tableauPlaceholder' id='viz1694383919591' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ho&#47;HousingSales_16943410889020&#47;ZIPCODE&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='path' value='views&#47;HousingSales_16943410889020&#47;ZIPCODE?:language=en-US&amp;:embed=true&amp;publish=yes' /> <param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ho&#47;HousingSales_16943410889020&#47;ZIPCODE&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div> 

From the King and County Dataset, we are able to see that: 
1. The sqt_living affects the house selling price. (The larger the sqt_living size the more the house is sold)

<div class='tableauPlaceholder' id='viz1694341669294' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ho&#47;HousingSales_16943410889020&#47;Sqft_livingVsPrice&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='HousingSales_16943410889020&#47;Sqft_livingVsPrice' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ho&#47;HousingSales_16943410889020&#47;Sqft_livingVsPrice&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>            

2. The different features (bathrooms, bedrooms) also affect the house selling price
<div class='tableauPlaceholder' id='viz1694341984205' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ho&#47;HousingSales_16943410889020&#47;FeaturesVsPrice&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='HousingSales_16943410889020&#47;FeaturesVsPrice' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ho&#47;HousingSales_16943410889020&#47;FeaturesVsPrice&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>        

## Modelling
For this project, we will require the use of multiple linear regression modeling to analyze house sales in a northwestern county. Multiple linear regression is a statistical technique used to determine the relationship among several random variables. 

For this project, we will use multiple linear regression, to help us understand and determine the relationship between multiple independent variables (house features) and the dependent variable, which in this case is House Sale Prices.

For the dataset represented: 
#### 1. Univariate Analysis
We conducted univariate analysis to understand the distribution and characteristics of individual variables.

*Results
For the univariate analysis of the dataset, the categorical data put into consideration include the 3 listed:
 Bedrooms
Bathroom
sqft_living.
We are able to conclude that from the count, the major features that attract customers to buy a house are like the above-listed

#### 2. Multivariate regression analysis
We conducted a multivariate analysis to understand the relationship between the house features and the price.

*Results
The size of the living area, indicated by sqft_living, has the strongest positive impact on property prices.
The number of bathrooms also significantly influences prices. Bedrooms, while still positively correlated, have a comparatively weaker impact. Other attributes like floors, sqft_living15, and yr_built show moderate correlations with various features.

<img src="image.jpeg" align="right" width="350px" height="250px" alt="Method" />

### Technologies Used
Based on what was learned, we were able to carry out the following:
1. Data Understanding
2. Data Cleaning and Preparation
3. Data Visualization
4. Exploratory Data Analysis
5. Data Modelling



## Regression Results
From the data modeling done in the previous step, below represent the regression analysis results of the King County DataSet.

Here we will run a baseline linear regression model using various features as predictors, including the number of bedrooms, bathrooms, square footage of living space, square footage of the lot, number of floors, waterfront status, house condition, and grade.

## Conclusion
<img src="https://media.giphy.com/media/UqqVRaP8y4uo1GNxbN/giphy.gif" width="720px" height="250px">
Negative Factors: The number of bedrooms (bedrooms) and the year built (yr_built) have negative coefficients. This implies that an increase in the number of bedrooms or an older year of construction may lead to lower house prices.

Less Impactful Factors: The square footage of the lot (sqft_lot), the number of floors (floors), and the condition of the property (condition) also play a role in house prices but to a lesser extent.

Customer satisfaction, knowing the above features have an influence on the buyer's decision, the stakeholder can advise on what renovations are most marketable.

### Recommendations
#### Based on the modeling techniques above, we are able to come up with the following insights:
Bedrooms: One of the predictor variables. Its coefficient is -0.0278, which indicates that for each unit increase in the number of bedrooms, the dependent variable (price) decreases by approximately 0.0278 units.

Bathrooms: This is another predictor variable. Its coefficient is 0.0890, indicating that for each additional bathroom, the dependent variable(price) increases by approximately 0.0890 units.
sqft_living: This is a predictor variable representing the square footage of living space. Its coefficient is 0.0002, suggesting that for each additional square foot of living space, the dependent variable(price) increases by approximately 0.0002 units.

sqft_lot: This is another predictor variable representing the square footage of the lot. Its coefficient is very small and negative (-2.002e-08), but it's not statistically significant since its p-value is 0.787, indicating that it may not be significant in terms of predicting price.

Floors: The coefficient for the "floors" variable is 0.0818. This suggests that holding all other variables constant, for each additional floor in a house, the predicted value of the dependent variable (e.g., house price) increases by approximately 0.0818 units.

Waterfront: The coefficient for the "waterfront" variable is 0.4698. Since "waterfront" is likely a binary variable (0 for no waterfront and 1 for waterfront), this coefficient indicates that having a waterfront property increases the predicted value of the dependent variable(price) by 0.4698 units compared to non-waterfront properties. 

Condition: The coefficient for the "condition" variable is 0.0405.
This suggests that holding all other variables constant, for each unit increase in the condition rating of a property, the predicted value of the dependent variable(price) increases by approximately 0.0405 units.

Grade: The coefficient for the "grade" variable is 0.2242. This indicates that holding all other variables constant, for each unit increase in the property grade rating, the predicted value of the dependent variable(price) increases by approximately 0.2242 units.

#### Based on the results above, we concluded that All the independent variables aside from sqft_lot have a p-value of 0.00 which indicates their significance in predicting price.

*Repository Structure*


├── data

    ├──column_names.md
    ├──kc_house_data.csv
    ├──kc_house_data.xlsx
    
├──Project_presentation.pdf
├── README       
├── image.jpeg
├── image1.jpeg
├──image2.png
├── student.ipynb

        

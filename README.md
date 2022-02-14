# KC House Data Insights
<p align="center">
<img src = "https://github.com/ElisaRMA/KC-House-Data-Insights/blob/master/observation-urban-building-business-steel.jpg" width="750">
</p>

_This logo is also fictional_

The business problem and the ‘House Rocket’ company portraited in this project are ficticional.

The resulting app can be accessed [here](https://kc-insights.herokuapp.com/)

## 1. **Project description and Business Problem**

House Rocket is a company based on King County - USA, based on buying, renovating and selling real estate. The main bottleneck, however, is how to select the best real estate opportunities in order to increase the profit. The best case scenario would be to buy good houses, at good conditions and locations, at a low cost to sell them at a higher price. 

The business questions/problems to be solved are: 

1. Which houses the company should buy and at which price?
2. Once bought, when should these houses be sold and at which profit margin?

## 2. **Business Assumptions**
    
In order to move along with this project some assumptions were made:
    
- Duplicate IDs were removed as they were considered data input mistakes. The records were added in duplicate at different time periods possibly due to human error, therefore only the last record was used.
- General location, being waterfront (or not), and housing condition were the most decisive characteristics to classify if a house should be purchased.
- The season was a decisive information for selling price. 


## 3. **Data Dictionary**

The data used in this project was obtained from [Kaggle](https://www.kaggle.com/harlfoxem/housesalesprediction/discussion/207885) and the columns correspond to the list below: 

- id - Unique ID for each home sold
- date - Date of the home sale
- price - Price of each home sold
- bedrooms - Number of bedrooms
- bathrooms - Number of bathrooms, where .5 accounts for a room with a toilet but no shower
- sqft_living - Square footage of the apartments interior living space
- sqft_lot - Square footage of the land space
- floors - Number of floors
- waterfront - A dummy variable for whether the apartment was overlooking the waterfront or not
- view - An index from 0 to 4 of how good the view of the property was
- condition - An index from 1 to 5 on the condition of the apartment,
- grade - An index from 1 to 13, where 1-3 falls short of building construction and design, 7 as an average level of construction and design, and 11-13 have a high quality level of construction and design.
- sqft_above - The square footage of the interior housing space that is above ground level
- sqft_basement - The square footage of the interior housing space that is below ground level
- yr_built - The year the house was initially built
- yr_renovated - The year of the house’s last renovation
- zipcode - What zipcode area the house is in
- lat - Lattitude
- long - Longitude
- sqft_living15 - The square footage of interior housing living space for the nearest 15 eighbors
- sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors

## 4. **Solution Strategy**

**Step 01.** Determining the business problem

**Step 02.** Load and Inspect the Data

**Step 03.** Clean and Transform the Data 

**Step 04.** Exploratory Data Analysis

**Step 05.** Business Hypothesis Testing 

**Step 06.** Answering the Business Questions 

**Step 07.** App creation 

**Step 08.**  Conclusion and Understanting the Business results

## 5. **Top Insights**

**H1 - Waterfront houses are 30% more expensive.**

False. Houses with waterview are 3 times **more** expensive than houses with no waterview. Therefore, investing in houses with a waterview at lower prices than usual, would be ideal. 

**H2 - Houses built before 1955 are 50% less expensive.**

False. apparently, the year of construction does not have significant effect. Invest in houses independently of the year of construction, taking into account other variables.

**H3 - Houses with a basement are 30% more expensive**

True. Invest in houses with a basement, with prices below the mean.

**H4 - The price of houses decrease 30% at every drop in condition**

False. Not every drop in condition had a significant effect on house prices. Investing in houses in condition 3 or better have no difference in price. 

**H5  - Houses in good condition (3 up) and good view (3 and 4) are 30% more expensive than houses in bad condition (1-2) and good view (3 and 4)**

False due to standard deviation. Good view interferes more with house prices than condition. Invest in houses in bad condition (cheaper) but good view, renovate them, and sell. 

**H6 - Houses with good view (3 and 4) are 30% more expensive than houses with a bad view (0 to 2)**

False. Houses with a good view are even **more** expensive. Invest in houses with a good view. 

**H7 - Houses with a smaller sqft_lot close to houses with a larger sqft_lot are 10% more expensive than the average**

False. No neighboorhood effect if taking into account the sqft_lot.

**H8 Houses with a smaller sqft_living close to houses with a larger sqft_living are 10% more expensive than the average**

True. Neighboorhood effect happens when taking sqft_living into account. Invest in houses close to bigger ones at low prices so that profit marge is higher. 

**H9 - The YoY rise in price is 10%**

False. Price decreased in 2015. 

**H10 - The MoM rise in prices of houses with 3 bathroom is 15%**

False. Prices decrease and increase at the period comprised in the dataset. The months of January, February and November would be the best moment to invest in houses.


## 6. **Business Results**

Based on the analysis done herein, 10486 houses were considered fit for purchase. 
Such houses had good conditions, were compared based on their location and if they were located in front of water or not.

By summing up the prices, if all 10486 houses were bought, the transaction cost would be $4116121077. For this case, the total profit if all houses were sold would be $755,904,284.5

If, however, only the houses with a profit margin of 30% were bought, a total of 5117 houses, the transaction cost would be $1721460884.0. In such case, the profit would be would be around $516,438,265.12

By choosing the second option, less then 50% of the suitable houses would be purchased but the resulting profit would represent 68% of the one obtained with all 10486. 


## 7. **Conclusions** 
The main objective of this project was to answer two business questions:
1. Which houses the company should buy and at which price?
2. Once bought, when should these houses be sold and at which profit margin?

To achieve this goal, the dataset was cleaned, analysed, and some hypothesis were tested. To determine the best real state opportunities, the data was grouped based on location, housing condition and if it was located in front of water. 

These features were determined based on previous analysis, in which it was observed that location played one of the most important role in house precification. Along with general location, if a house was near a body of water, its price would also increase. In addition, for all these situations, the housing condition, specially the on lower grades, presented a proeminent effect on prices, decreasing them significantly. 

After grouping the houses on the dataset based on these conditions, the average price was calculated and if a house costed less then this average and it was in good condition, this house would be classified as suitable for purchase. After separating all suitable houses, the profit was calculated. 

This calculation was done by grouping the good real state opportunities based on all previous features and season. The average prices were calculated and if the buying price were above this average, a profit margin of 10% would be added, otherwise, the profit margin would be at 30%.

At the end of such analysis, the resulting dataset contained 10486 houses, its features, the buying and selling prices and the profit margin of each. 

## 8. **Next Steps**

This project was done following the minimal viable product (MVP) concept. The analysis done herein is very simple but offer a good start on a similar business problem. The next steps would be to improve such analysis by applying more sofisticated methods. 

First, a statistical analysis could be done on the business hypothesis testing, to verify if the results found really were significant. Next, further feature engeneering could be done and a machine learning model could be constructed to determine the best opportunities, moments and price to sell such houses. 

The implementation of machine learning algorithm could start with simple regression models and evolve to the use of random forest or more complex, models.  

> _This project was done following the context and suggestions offered in the [Seja um Data Scientist](https://sejaumdatascientist.com/os-5-projetos-de-data-science-que-fara-o-recrutador-olhar-para-voce/) blog_

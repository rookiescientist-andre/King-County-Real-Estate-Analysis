# King County Real Estate Analysis

**Author**: Andre Layton  
GitHub: @therookiescientist-andre

## Overview

  Despite mortgage interest rates climbing to a record high in the last 35 years, the United States is continuing to see a seller's market, where there is a higher demand for purchasing a home than there are homes available to buy. Now, selling a home may sound daunting, but once the home is priced and listed for sale, you want to ensure you get the highest value possible. Increasing this potential value can be as easy as making minor aesthetic upgrades, such as painting the walls, or major changes, such as a complete kitchen remodel. This project aims to give sellers an idea of what renovations in particular will increase the sales price of the home, and to estimate how much those renovations impact the home's value. 
  
## Business Problem

  A homeowner has a property in northwest Washington that they are looking to sell. However, they have no prior experience in real estate, and they want to be sure they are not missing out on a chance to maximize their return. They recognize that working with a real estate agent will help their profit potential, and making changes to the home prior to listing it will do the same. Therefore, the homeowner would like to know what potential renovations will increase the property value. I am analyzing housing data from King County, WA in order to identify what opportunities there are to increase the sales price of the home, and by how much. 
***

## Data & Methods

  The data analysed came from the King County government website. The dataset lists a full record of all the homes in the King County, WA area, and their corresponding features (i.e., size, price, floors, and etc.). The dataset is a combination of both numeric and categorical features, and will be studied to find which features in particular would have the best impact on sales price, and then help determine what renovations to focus on.

  After I explore the dataset and the distribution of the sales price, I clean up the dataframe by renaming columns and "dummying" out the heat sources column, in particular, in order to begin finding correlations and relationships. I use a heatmap to best show how each feature interacts with the sales price of the homes, and begin my feature selection process.
  
  ![Heatmap with Correlation Coefficients](images/heatmap.png)
  
The heatmap shows that the size of the living space (in square feet) is the feature that is highly correlated with sales price, and is a predictor worth exploring. I also apply the Recursive Feature Elimination (RFE) method, which suggests a look into the heating sources, specifically electricity. 
***

## Modeling

  The first few plots explore a simple linear regression model between the size of the living space (in sq. ft.) and the sales price of the home. After dropping the outliers using the interquartile range (IQR) method, we plot the data along with a best-fit line to observe the effect our predictor has on the target. 
  
  ![Sq. Ft. of living space vs. sales price](images/sqft_reg.png)
  
  The visual above shows that there is a strong linear relationship between the size of the living space and the sales price of the home. The model's adjusted R-squared statistic is .318 - in other words, the size of the living space explains about 32% of the variance in the sales price. The residuals are also plotted, as shown below, and exhibit a semblance of a normal distribution, which confirms that no assumptions were violated. 

  ![Residuals visual](images/sqft_resid.png)

  The next few visuals take a look into the heating sources and their impact on the sales price of the home. This data takes a different process due to its categorical nature, so a visual of the data's distribution is important. The first plot is a bar graph showing the median sales prices for each heating source.
  
  ![Heating Sources vs. median sales price](images/heatsources.png)

  Median gas-powered homes were much higher than electric-powered homes, as well as oil. The model explains about 3% of the variance in the sales price, which is quite small. This inspires little confidence in the results and any interpretations to the relationship between both variables The model suggests that, when compared to electric-powered homes, the home's sales price is estimated to increase by $180,400 for gas-powered homes and $33,660 for oil-powered homes. 
  
  The last few visuals model all the individual predictors together, in order to achieve model improvement and observe what impact the predictors have on the sales price when factored in, completely. The model shows little improvement in the adjusted R-squared statistic (a value of 0.319), when compared to the size of living space's simple linear model, yet the coefficients are statistically significant. The mean absolute error is $279,239, which is how much our model is off by in any given prediction. This is quite high and warrants improvements for future analysis.  

***



## Results & Conclusions

This analysis leads to the following conclusions:

1. Before listing the home, increase the living space of the home. Each square foot that gets added to the living space is projected to increase the price of the home by approximately \\$302. Increasing the square footage of the living space is confirmed to have the greatest impact to the sales price of the home, but is collinear with many other features and must, therefore, be modeled with a few select predictors.

2. If the home is electric-powered, and there is definite interest in changing the heating system of the property, I recommend renovating to a gas-powered home. Firstly, the median gas-powered home is priced much higher than the median electric and oil- powered home. As compared to electric power,  gas-powered homes are estimated to see an increase in price, on average, by \\$97,000, which is the highest among the heating sources present in the model. However, under normal circumstances, I would not recommend remodeling the heating system. The model suggests that the heating sources actually have a weak influence on a property's value, and inspires little confidence or credibility. 

This project is limited in a few ways, the first being it only takes into account housing data within the upper and lower bounds of the dataset. In addition, the features that correlated best with the sales price also exhibited strong relationships with one another. This limited the amount of features we could include and analyze, and warrant further, individual looks to observe any possible improvements to our model.

Further analyses could yield additional insights to which features and/or renovations are best to impact the sales price of the homes in the Pacific Northwest region. One such improvement is including location into the project to see the impact area has on price. Also, include more features to explore other predictors that may correlate better with the sales price of the home. 

***





## Repository Contents
***
Below is a list of the contents of this repository.

```
├── README.md             
├── images   
├── .gitignore
├── RealEstateAnalysis.ipynb                               
└── Presentation.pdf                         
```

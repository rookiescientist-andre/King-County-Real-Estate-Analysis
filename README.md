# King County Housing Data Analysis

**Author**: Andre Layton

GitHub: @therookiescientist-andre

## Overview

  Keller Williams Realty has acquired some new property that they are looking to put on the market and sell within the next 1-2 years. Houses in their inventory are allotted more time before reselling, but this is their first property in the Pacific Northwest, and the company would like to use this project to aid in expanding their business into that region. This project aims to give Keller Williams an idea on what specific renovations they need to focus on in order to drive the sales price higher and by how much.
  
## Business Problem

  Keller Williams Realty would like to know what individual renovations will be necessary to increase the property's sales price prior to listing the house for sale. The company would also like to know how much of an impact the heating sources have on the property's value, and whether it is significant enough to consider for renovation. In order to identify which renovations should take priority, I am analyzing housing data from King County, WA in order to find these features and gain a better understanding of which features are the best predictors of sale price.
***

## Data & Methods

  The data analysed came from the King County government website. The dataset lists a full record of all the homes in the King County, WA area, and their corresponding features (i.e., size, price, floors, and etc.). The dataset is a combination of both numeric and categorical features, and will be studied to find which features in particular would have the best impact on sales price, and then help determine what renovations to focus on.

  After I explore the dataset and the distribution of the sales price, I clean up the dataframe by renaming columns and "dummying" out the heat sources column, in particular, in order to begin finding correlations and relationships. I use a heatmap to best show how each feature interacts with the sales price of the homes, and begin my feature selection process.
  
  ![Heatmap with Correlation Coefficients](images/heatmap.png)
  
The heatmap shows that the size of the living room (in square feet) is the feature that is highly correlated with sales price, and is a predictor worth exploring. The business problem initially has interest in the homes' heat sources, which adds another feature to the project.   
***

## Results

  The first few plots depict the median ROIs on both scopes, as well as the average Worldwide ROI by genre, which we later refined our analysis view to. All three plots support that Adventure films are the best type to begin creating among the top four mentioned earlier, with Comedy coming in second, as measured through this analysis. This would also invite conversations of merging the two genres, given the dataset initially had multiple genres. 

  The next few visuals - the boxplot and multiple regression plots - exhibit how production budgets vary among the top four genres, and the bar chart shows that the Adventure films in the dataset required $70 million for production, on average. However, I am suggesting a production budget between $100-140 million, in order to potentially generate four times the investment (at minimum a triple return on invesmtment).

  The final boxplot statistically, and visually, breaks down the runtime among the top four genres. A runtime between 95-110 minutes would be best for this initial project, which would cover the 75th percentile of Adventure films as well as Comedy films if we were to further suggest merging genres for the screenplay, as mentioned earlier. 

To improve confidence in the results next time I would:

  Include the movie ratings and refine to include multiple genre characterizations in order to give a clear, more comprehensive picture of the dataset. In addition, research when might be the best time to release to give a refined projection/plan.

***



## Conclusions

This analysis leads to three recommendations regarding types of movies that are best to begin creating:

1. START WITH ADVENTURE-COMEDY FILMS. Adventure films generate the highest median worldwide return on investment, among the top four genres. We focused our analysis to those four genres due to a lack of records for the other genres, and their susceptibility to outliers (e.g., low budget films that found major success), to confidently include them in the analysis. As such, Adventure films were the best choice to begin with, and is estimated to produce both the highest median and average worldwide returns - suggesting the film will make enough to cover production costs and even generate profit. I would further suggest merging genres with Comedy for the screenplay, which will allow us to draw from different demographics and markets to gain success/following from. Therefore, an Adventure-Comedy film.

<img src="images/average_worldwide_roi.png" alt="Production Budget by Genre">
    
2. BUDGET SUGGESTIONS. According to the average budget and Worldwide ROI visuals above, prepare to spend a minimum of $70 million on this film in order to double the return on investment. However, I am suggesting a budget plan between $100-140 million, in order to make, approximately, three times the budget at the minimum and a ceiling projected at quadruple the investment. 

![Production Budget by Genre](images/budget_boxplot.png)

3. RUNTIME SUGGESTIONS. I am suggesting a minimum runtime of approximately 95 minutes for the Adventure film. However, if we follow my earlier suggestion regarding merging genres, an Adventure-Comedy film would require a runtime between 95-110 minutes. 

![Runtime by Genre](images/runtime_boxplot.png)

***





## Repository Contents
***
Below is a list of the contents of this repository.

```
├── README.md             
├── images   
├── .gitignore         
├── KingCountyHousingDataAnalysis.ipynb                               
└── King County Housing Data Analysis.pdf                         
```

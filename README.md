## The Pursuit of Happiness, a Group Project.
Think money can buy you happiness? Read on to see if there's truth to that.. 

Applying data analytics and visualization techniques to highlight other factors that impact world happiness.


<div align="center">
  
![World Intro](https://user-images.githubusercontent.com/65078870/86182388-de762b80-bafd-11ea-91fc-d45ea06165aa.gif)

</div>

## Introduction

The United Nations (UN) General Assembly passed a resolution in 2011 that said “the pursuit of happiness is a fundamental human goal”. It called on governments to "give more importance to happiness and well-being in determining how to achieve and measure social and economic development." 

Now it might seem an odd time to start a project about world happiness. After all, how can someone be really happy during a global pandemic? 

But we've all thought that we'd be happier with more cash in our pocket at some point or another; and it's only natural to feel unhappy and stressed when money's tight. This is precisely why now is the right moment to explore readily available data, to be able to analyze trends over time and correlate factors that impact happiness across the world. 

While some would argue that “Rich countries are definitely happier than underdeveloped countries,” this project evaluates the importance of other factors, in addition to a country's economic health.

## Mission

Utilize Python, Pandas, Numpy and, Matplotlib and other visualization libraries to analyze and answer the following questions: 

+  [How does the Happiness Index vary across the globe?](#happiness-index-across-the-globe)
+  [Does economic health correlate with happiness?](#economic-health-factors-versus-happiness-index) 
+  [What other factors impact happiness?](#summary-of-correlations)
+  [How do happy countries relative to their economic health rank on the Happiness Index variables?](#outliers-and-happiness-index-variables)
+  [How do happy countries relative to their economic health rank on other factors correlated with happiness?](#outliers-and-other-factors)
+  [How does Canada perform on the Happiness Index variables and how does it compare to the US?](#canada-and-usa-on-happiness)
+  [Is happiness changing over time?](#happiness-over-time) 

## Data Background

Our primary dataset was obtained from the World Happiness Report (WHR) developed by UN's Sustainable Development Solutions Network. It's an annual publication that surveys the state of global happiness and ranks countries by how happy their citizens perceive themselves to be and by various life factors. 

The group also searched for other factors that could potentially impact the measure of happiness. Additional datasets were obtained from different sources including the Global Health Data Exchange (GHDx) by the University of Washington, The Global Economy, Central Intelligence Agency (CIA) Government, and World Economic Forum. 

<div align="center">
  
<img width="459" alt="Sources Tablev2" src="https://user-images.githubusercontent.com/65078870/86791381-782a6500-c037-11ea-8f9f-055f91686eca.PNG">

</div>

Most retrieved datasets date back to 2005, although the first official WHR was published in 2012. The scope of this analysis is predominantly the year 2017, as this is the most recent year that provided a near complete picture within the Happiness Index dataset and the additional variables analyzed. 

## Hypothesis

"A country's economic health by measure of GDP and Unemployment does not impact the happiness of its people"


## Data Cleaning
  
Datasets were downloaded in the form of Comma Separated Values (CSV). The data cleaning process began with renaming column headers and dropping columns not required for the analysis. Datasets were not always complete, therefore fields containing NaN values were replaced with the preceding or succeeding year's values. Data from various sources were merged to create a complete dataset for analysis. Merging from different sources created the challenge of dealing with country names that did not match in all data sets. Therefore the match function was used to identify the same countries with different names, followed by renaming to create a complete set of matching country names across all data sets. Finally all data points were transformed through a function matrix and merged into a single dataframe. To find correlation and to be able to compare rankings and performance among the various variables, the values in each happiness-related factors were normalized for the analysis.

[See code: Data Cleaning](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/July07_vivi/DataCleaning.ipynb)

## Data Analysis

An initial exploratory analysis of the data was conducted during the "pre-work" phase in order to frame the specific questions that this project sought to answer. Once the group identified specific factors and outlier countries of interests to focus on, the main analysis proceeded. The group looked at the correlation among identified variables with happiness and conducted a deep-dive into what other factors could be impacting happiness among the countries of focus, including Canada. 

## Data Visualization 

[See Code: Analysis and Visualization](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/Analysis/Consolidated%20Visualizations.ipynb)

<!-- toc -->

### Happiness Index Across the Globe

Click below image to be directed to the html file for download and to view an interactive version of the globe:


<div align="center">
  
  [![Globe Happiness viz gif](https://user-images.githubusercontent.com/65078870/86514330-bc232d00-bddf-11ea-8772-b974bd960f6e.gif)](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/images/Fig_Q1.html)
  
</div>


## In Focus: Analysis
  
  ### Economic Health Factors and the Happiness Index
  #### **_Does economic health correlate with happiness?_** 
  
  <div align="center">
  
  <img width="681" alt="EconomicHealth vs Happiness correlation" src="https://user-images.githubusercontent.com/65078870/86192663-168a6800-bb18-11ea-8708-82530e2e6ab8.PNG">
  
  </div>
  
 
  <div align="center">
  
  <img width="687" alt="EconomicHealth vs Happiness Outliers" src="https://user-images.githubusercontent.com/65078870/86192733-3faaf880-bb18-11ea-988b-32d28f248158.PNG">
  
  </div>
  
   
   **_Observable Trends/Insights:_** 
  
  +   To analyze economic health and it's correlation to the Happiness Index, we looked at GDP and % unemployment as indicators of economic health. Pearson correlation coefficient found that GDP is highly correlated with the Happiness Index (r=0.74), while % unemployment had a much weaker correlation with the Happiness Index (r=-0.21). 
    
  +   A regression analysis helped identify select countries that were relatively happier in comparison to their economic health. We identified and focused on **Costa Rica** and **Nicaragua** who had a relatively high happiness index score while lower GDP, and **Brazil** and **Spain** who also had a relatively high happiness index score while higher % of unemployment. 
  
  ----
  
  ### Additional Factors that Impact Happiness
  
  #### **_What other factors are correlated with the Happiness Index?_** 
  A series of variables (17 additional) from different datasets were compiled and analyzed for correlation with the Happiness Index
  
  <div align="center">
  
  <img width="846" alt="Series Variable Correlation v2" src="https://user-images.githubusercontent.com/65078870/86848813-b138f880-c07c-11ea-929a-a9e125f34556.PNG">
  
  </div>
  
  
   **_Observable Trends/Insights:_** 
   
   +  **Brain drain** and **Security index** topped the negatively correlated factors that impact Happiness. 
   +  **Sleep** and  **Literacy rate** topped the positively correlated factors that impact Happiness. While Sleep and Literacy rate were highly correlated, due to limited data availability, we shifted our focus to the next two positively correlated factors: **Tourism revenue** and **Average age of population**

  ----
  
  ### Relatively Happy Countries and Their Performance on Happiness Index Variables
  #### **_How do our focus countries rank on the Happiness Index variables?_** 
  
  <div align="center">
  
  <img width="692" alt="Happy Outliers and Happiness Index2" src="https://user-images.githubusercontent.com/65078870/86754156-a8a9d900-c00e-11ea-97a3-3d67fa52efb5.png">
  
  </div>
  
  
   **_Observable Trends/Insights:_** 
   
   +  Scores vary along the Happiness Index factors among selected happy countries. All countries showed high scores for **Social Support**. 
   
   +  Costa Rica and Nicaragua scored especially high on **Freedom**, while Spain scored high on **Healthy Life Expectancy**.  
   
   +  Interestingly, these selected countries ranked low on **Generosity**.  
  
  ----
  
  ### Relatively Happy Countries and Their Performance on Other Factors Related to Happiness
  #### **_How do our focus countries rank on additional factors found to be correlated with the Happiness Index?_**  
  
  <div align="center">
  
  <img width="917" alt="Top Factors for Happy and Unhappy" src="https://user-images.githubusercontent.com/65078870/86612584-5e791700-bf7e-11ea-8825-1435c6b6da55.PNG">
  
  </div>
  
  
  **_Observable Trends/Insights:_** 
  +   Scores for additional variables correlated with happiness vary among the selected happy countries. Interestingly, Nicaragua does not perform well across all four variables.
  
  +   Spain has the highest earnings from tourism, while other focus countries underperformed on this indicator. 
  
  +   Brain drain is a challenge for these countries - maximum brain drain occurs in Nicaragua. Security threat could be one of the major reasons for impacting the perception of happiness.
  
  
  
  ----
  
  ### Canada and US on Happiness
  #### **_How does Canada rank on the Happiness Index variables and additional factors found to be correlated with happiness?_**  
  
  <div align="center">
  
  <img width="344" alt="Canada Vs US GDP" src="https://user-images.githubusercontent.com/65078870/86613852-21158900-bf80-11ea-90d9-f3405ac7bb34.PNG"><img width="450" alt="Canada vs US Happiness" src="https://user-images.githubusercontent.com/65078870/86755096-603eeb00-c00f-11ea-94bf-ad1a6eeb1ab3.PNG">
  
  </div>
  
  
  **_Observable Trends/Insights:_** 
  +   With the exception of GDP & Generosity, Canada out performs the US across Happiness Index variables. 
  +   Perception of corruption is especially low in Canada compared to the US. This clearly demonstrates that GDP is not everything when it comes to a nation's Happiness Index. 
  
  ----
  
  ### Happiness Over Time 
  ### **_Is happiness changing over time?_** 
  
  <div align="center">
  
  <img width="474" alt="Happiness over time" src="https://user-images.githubusercontent.com/65078870/86614812-8cac2600-bf81-11ea-94fa-c626a4f800a3.PNG">
  
  </div>
  
  
  **_Observable Trends/Insights:_** 
  +   Globally, happiness as defined by the Happiness Index is relatively stable. 
  +   Although, among the selected countries we looked at, Nicaragua has been trending happier in more recent years while Spain’s happiness has been slowly declining.

  <div align="center">
  
  <img width="468" alt="Canada Happiness over time" src="https://user-images.githubusercontent.com/65078870/86615248-32f82b80-bf82-11ea-9dd5-6f24866d968b.PNG">
  
  </div>
  
  +   As for Canada -- happiness as defined by the Happiness Index has been relatively stable in Canada over the 10-year analysis period. 
  
  ---
  
  
  
  # Conclusions
  +   Economic health is positively correlated with a nation’s happiness - namely a nation's GDP is found to be highly correlated with the Happiness Index (r=0.74)
  +   While economic health is a positive indicator for happiness, additional factors were identified to also be highly correlated with happiness. Negatively correlated: Brain drain and Perception of security; positively correlated: Literacy rate, Average amount of sleep, Average population age, and Tourism revenue. 
  
  # Limitations
  +   Happiness was defined as per the World Happiness Report and therefore we were limited to this definition and the algorithm used by the UN in conducting and evaluating happiness across the globe. 
  +   We were limited to the variables we examined to determine _other_ factors that may be correlated with happiness. There are other measures by which we can examine economic health, in addition to GDP and unemployment rate. In addition to looking at economic health other studies in this area have looked at factors such as weather, culture, religion, and fun to determine whether these have an impact on a nation's level of happiness. 
  +   We used multiple data sets from various sources to examine the _additional_ variables that may be correlated with the primary data set from the Happiness Report. As we cleaned and merged differet data sets together we were limited to the common sets of information available and therefore this limited our findings for certain countries and timeframes. Therefore another limitation of this analysis was due to the inherent incompleteness of some the data we had access to, namely for global literacy rate and amount of sleep. 
  
  # Appendices
  
  Powerpoint Presentation:
  + [Slides](https://github.com/SShojaie/Suicide_squad/blob/master/Powerpoints/Project%20Week_Pursuit%20of%20Happiness_v1.0.pptx)
  
  Jupyter Scripts:
  + [Cleanup and Analysis Codes](https://github.com/SShojaie/Suicide_squad/tree/master/PursuitOfHappiness/Codes)
  
  Saved Figures:
  + [Images](https://github.com/SShojaie/Suicide_squad/tree/master/PursuitOfHappiness/Images)
  
  Raw Data and Outputs:
  + [Datasets](https://github.com/SShojaie/Suicide_squad/tree/master/PursuitOfHappiness/Data)
  
  Reference/Sources: 
  + https://worldhappiness.report
  + https://ghdx.healthdata.org
  + https://www.theglobaleconomy.com
  + https://www.cia.gov/library/publications/the-world-factbook/rankorder/2177rank.html
  + https://www.weforum.org/agenda/2019/04/which-countries-get-the-most-sleep-and-how-much-do-we-really-need
  

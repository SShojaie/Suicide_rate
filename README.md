## The Pursuit of Happiness, a Group Project.
Think money can buy you happiness? Think again. 

Applying Data Analytics and Visualization Techniques to highlight other factors that impact world happiness.


<div align="center">
  
![World Intro](https://user-images.githubusercontent.com/65078870/86182388-de762b80-bafd-11ea-91fc-d45ea06165aa.gif)

</div>

## Introduction

The United Nations (UN) General Assembly passed a resolution in 2011 that said “the pursuit of happiness is a fundamental human goal”. It called on governments to "give more importance to happiness and well-being in determining how to achieve and measure social and economic development." 

Now it might seem an odd time to start a project about world happiness. After all, how can someone be really happy during a global pandemic? 

But we've all thought that we'd be happier with more cash in our pocket at some point or another; and it's only natural to feel unhappy and stressed when money's tight. This is precisely why now is the right moment to explore readily available data, to be able to analyze trends over time and correlate factors that impact happiness across the world. 

While some would argue that “Rich countries are definitely happier than underdeveloped countries,” this project will look into other variables other than a country's economic health.

## Mission

Utilize Python, Pandas, Numpy and Data Visualization tools to answer the following questions: 

+  [How does the happiness index look across the globe?](#happiness-index-across-the-globe)
+  [Does economic health correlate with happiness?](#economic-health-factors-versus-happiness-index) 
+  [What other factors impact happiness?](#summary-of-correlations)
+  [How do relatively happy countries rank on the Happiness Index variables?](#outliers-and-happiness-index-variables)
+  [How do relatively happy countries rank on other factors?](#outliers-and-other-factors)
+  [How does Canada perform and compare to US?](#canada-and-usa-on-happiness)
+  [Can happiness change over time?](#happiness-over-time) 

## Data Background

Our primary dataset was obtained from the World Happiness Report (WHR) developed by UN's Sustainable Development Solutions Network. It's an annual publication that surveys the state of global happiness and ranks countries by how happy their citizens perceive themselves to be, which the report also correlates with various life factors. 

The group also searched for other factors that could potentially impact the measure of happiness. Those datasets were derived from different sources such as the Global Health Data Exchange (GHDx) by the University of Washington, The Global Economy, Central Intelligence Agency (CIA) Government and World Economic Forum websites. 

<div align="center">
  
<img width="454" alt="Sources Table" src="https://user-images.githubusercontent.com/65078870/86603006-75653c80-bf71-11ea-8f1b-f6388edb3ba0.PNG">

</div>

All retrieved datasets date back to year 2005 but the first official WHR was published in 2012.  The scope of our in depth analysis covers the recent 2017 because it has a complete set of data. 

## Hypothesis

"A country's economic health by measure of GDP and Unemployment does not impact the happiness of its people"


## Data Cleaning
  
The datasets were downloaded in the form of Comma Separated Values (CSV). Data cleaning process began with renaming column headers, dropping columns not required for the calculation. The datasets were not always complete, so the fields that contained NaN values were replaced with the preceding and succeeding year values.  Since the various datasets were combined, the countries name in the data sets were not the same, so the match function was used to identify the same countries with different naming and were renamed. Subsequently, all data points were transformed through a function matrix and merged into a single dataframe. To find the correlation and compare among the various variables, the values were normalized during the analysis.

[See code: Data Cleaning](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/July06_cleanup/DataCleaning.ipynb)

## Data Analysis

An initial data analysis was conducted during the "pre-work" phase in order to reframe specific questions this project intends to pursue. When the group had identified certain factors and outlier countries of interests to focus on, the main analysis proceeded with correlation and regression of variables among those highlighted countries. 

## Data Visualization 

[See Code: Analysis and Visualization](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/Analysis/Consolidated%20Visualizations.ipynb)

<!-- toc -->

### Happiness Index Across the Globe

Click below image to be directed to the html file for download and view a more interactive visualization:


<div align="center">
  
  [![Globe Happiness viz gif](https://user-images.githubusercontent.com/65078870/86514330-bc232d00-bddf-11ea-8772-b974bd960f6e.gif)](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/images/Fig_Q1.html)
  
</div>


## In Focus: Analysis
  
  ### Economic Health Factors versus Happiness Index
  #### **_Does economic health correlate with happiness?_** 
  
  <div align="center">
  
  <img width="681" alt="EconomicHealth vs Happiness correlation" src="https://user-images.githubusercontent.com/65078870/86192663-168a6800-bb18-11ea-8708-82530e2e6ab8.PNG">
  
  </div>
  
 
  <div align="center">
  
  <img width="687" alt="EconomicHealth vs Happiness Outliers" src="https://user-images.githubusercontent.com/65078870/86192733-3faaf880-bb18-11ea-988b-32d28f248158.PNG">
  
  </div>
  
   
   **_Observable Trends/Insights:_** 
  
  +   Regression analysis finds bought GDP and Unemployment Rate are correlated with the Happiness Index, however there are exceptions. 
  
  +   GDP had a strong positive relationship or correlation with Happiness Index while Unemployment Rate inversely showed a negative correlation. 
  
  +   Exceptions include outlier countries namely  **Costa Rica** and **Nicaragua** beacuse it demonstrated relatively high Happiness Index scores even if its Log GDP were not outstanding. On the other hand, **Brazil** and **Spain** aldo had high Happiness Index scores in the midst of high unemployment rates.
   
  
  ----
  
  ### Summary of Correlations 
  
  #### **_What other factors impact happiness?_** 
  A series of variables (17 additional) from different datasets were compiled and analyzed for correlation with the Happiness Index
  
  <div align="center">
  
  <img width="892" alt="Series Variable Correlation" src="https://user-images.githubusercontent.com/65078870/86611437-a7c86700-bf7c-11ea-9d7f-d714f73881de.PNG">
  
  </div>
  
  
   **_Observable Trends/Insights:_** 
   
   +  **Brain drain** and **Security index** topped the negatively correlated factors that impact Happiness. 
   +  Although **Sleep (min)** and  **Literacy rate** showed the most positively correlated factors with Happiness Index, we looked into **Rev Tourism** and **Average Age** variables for further analysis beacuse it doesn't have the limitations imposed by the aforementioned factors. 
  ----
  
  ### Outliers and Happiness Index Variables
  #### **_How do our relatively happy countries rank on the Happiness Index variables?_** 
  
  <div align="center">
  
  <img width="692" alt="Happy Outliers and Happiness Index2" src="https://user-images.githubusercontent.com/65078870/86754156-a8a9d900-c00e-11ea-97a3-3d67fa52efb5.png">
  
  </div>
  
  
   **_Observable Trends/Insights:_** 
   
   +  Scores vary along the Happiness Index factors among selected happy countries. All countries showed high scores for **Social Support**. 
   
   +  Costa Rica and Nicaragua scored especially high on **Freedom**, while Spain scored high on **Healthy Life Expectancy**.  
   
   +  Interestingly, these selected countries rank low on **Generosity**.  
  
  ----
  
  ### Outliers and Other Factors
  #### **_How do our relatively happy countries rank on additional happiness variables, correlated with the Happiness Index?_**  
  
  <div align="center">
  
  <img width="917" alt="Top Factors for Happy and Unhappy" src="https://user-images.githubusercontent.com/65078870/86612584-5e791700-bf7e-11ea-8825-1435c6b6da55.PNG">
  
  </div>
  
  
  **_Observable Trends/Insights:_** 
  +   Scores for additional variables correlated with happiness vary among the selected happy countries. Interestingly, Nicaragua does not perform well across all four variables.
  
  +   Spain has the highest earnings from Tourism, while all other outlier countries underperform on this indicator. The average age of the outlier countries is low indicating that younger population perform better on happiness index and these factors are positively corelated to happiness index.
  
  +   Brain drain is a challenge for these countries, maximum brain drain occurs in Nicaragua, affecting its happiness index. Security threat could be one of the major reasons for impacting the perception of happiness, therby brain drain and security threat negatively impact the happiness index.
  
  
  
  ----
  
  ### Canada and USA on Happiness
  #### **_How do we (Canada) rank along the Happiness Index factors and the additional highly correlated variables?_**  
  
  <div align="center">
  
  <img width="344" alt="Canada Vs US GDP" src="https://user-images.githubusercontent.com/65078870/86613852-21158900-bf80-11ea-90d9-f3405ac7bb34.PNG"><img width="500" alt="Canada vs US Happiness" src="https://user-images.githubusercontent.com/65078870/86755096-603eeb00-c00f-11ea-94bf-ad1a6eeb1ab3.PNG">
  
  </div>
  
  
  **_Observable Trends/Insights:_** 
  +   With the exception of GDP & Generosity, Canada out performs the US across Happiness Index variables. Perception of corruption is especially low in Canada, compared to the US. This clearly demonstrates that GDP is not the most dominant factor in measuring a country's happiness index. 
  
  ----
  
  ### Happiness Over Time 
  ### **_Can happiness change over time?_** 
  
  <div align="center">
  
  <img width="474" alt="Happiness over time" src="https://user-images.githubusercontent.com/65078870/86614812-8cac2600-bf81-11ea-94fa-c626a4f800a3.PNG">
  
  </div>
  
  
  **_Observable Trends/Insights:_** 
  +   Globally, happiness as defined by the Happiness Index is relatively stable. 
  +   From our selected happy countries, Nicaragua has been trending happier in more recent years, while Spain’s happiness has been slowly declining 

  <div align="center">
  
  <img width="468" alt="Canada Happiness over time" src="https://user-images.githubusercontent.com/65078870/86615248-32f82b80-bf82-11ea-9dd5-6f24866d968b.PNG">
  
  </div>
  
  +   Canada’s Happiness Index has been relatively stable. 
  
  ---
  
  
  
  # Conclusion
  +   Reject the null hypothesis 
  +   Economic health is positively correlated with a nation’s Happiness Index
  +   Money doesn’t necessarily buy happiness, but it helps
  
  # Limitations
  +   Lietracy Rate and Sleep shows much stronger positive corelation with happiness index, but due to the unavilability of the data for the outlier countries, the in-depth analysis could not be performed using these two variables.
  
  # Appendices
  
  Powerpoint Presentation:
  + [Slides](https://github.com/SShojaie/Suicide_squad/blob/master/Powerpoints/Project%20Week_Pursuit%20of%20Happiness_v0.5.pptx)
  
  Jupyter Scripts:
  + [Pre-work Codes](https://github.com/SShojaie/Suicide_squad/tree/master/PursuitOfHappiness/Codes)
  
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
  

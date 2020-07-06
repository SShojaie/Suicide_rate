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

While some would argue that “Rich countries are definitely happier than poor countries,” this project will look into other variables other than a country's economic health.

## Mission

Utilize Python, Pandas, Numpy and Data Visualization tools to answer the following questions: 

+  [How does the happiness index look across the globe?](#happiness-index-across-the-globe)
+  [Does economic health correlate with happiness?](#economic-health-factors-versus-happiness-index) 
+  [What other factors impact happiness?](#summary-of-correlations)
+  [How do outlier countries perform within the UN's happiness index variables?](#outliers-and-happiness-index-variables)
+  [How do outlier countires perform with other factors?](#outliers-and-other-factors)
+  How does Canada compare with outlier countries? 
+  [How does Canada compare to US?](#canada-and-usa-on-happiness)
+  [How does happiness change over time?](#happiness-over-time) 

## Data Background

Our primary dataset is derived from annual World Happiness Reports (WHR) published by the UN's Sustainable Development Solutions Network. The other datasets were obtained from various sources through the following websites: 
+   https://ghdx.healthdata.org
+   https://www.theglobaleconomy.com
+   https://www.cia.gov/library/publications/the-world-factbook/rankorder/2177rank.html
+   https://www.weforum.org/agenda/2019/04/which-countries-get-the-most-sleep-and-how-much-do-we-really-need/

It is then merged with other data obtained from the GHDx (Global Health Data Exchange) by the University of Washington,  The World Bank, ... and

from various sources like world bank website, GDHx (University of Washington) and CIA website.

<div align="center">
  
<img width="460" alt="Datasets Table" src="https://user-images.githubusercontent.com/65078870/86512748-cc80db00-bdd2-11ea-89e7-6176e20802ea.PNG">

</div>

## Hypothesis

"Economic Health in terms of GDP and Unemployment are not correlated to Happiness"
  
"Other factors (variables exclusive of UN's WHR) do not impact Happiness"
  
## Data Cleaning
  
The datasets were downloaded in the form of Comma Separated Values (CSV). Data cleaning process began with renaming column headers, dropping columns not required for the calculation. The datasets were not always complete, so the fields that contained NaN values were replaced with the preceding and succeeding year values.  Since the various datasets were combined, the countries name in the data sets were not the same, so the match function was used to identify the same countries with different naming and were renamed. Subsequently, all data points were transformed through a function matrix and merged into a single dataframe. To find the correlation and compare among the various variables, the values were normalized during the analysis.

## Data Analysis

An initial data analysis was conducted during the "pre-work" phase in order to reframe specific questions this project intends to pursue. When the group had identified certain factors and outlier countries of interests to focus on, the main analysis proceeded with correlation and regression of variables among those highlighted countries. 

## Data Visualization 

<!-- toc -->

### Happiness Index Across the Globe

Click below image to be directed to the html file for download and to view an interactive visualization:


<div align="center">
  
  [![Globe Happiness viz gif](https://user-images.githubusercontent.com/65078870/86514330-bc232d00-bddf-11ea-8772-b974bd960f6e.gif)](https://github.com/SShojaie/Suicide_squad/blob/master/PursuitOfHappiness/Codes/images/Fig_Q1.html)
  
</div>


## In Focus: Analysis
  
  ### Economic Health Factors versus Happiness Index
  #### Does economic health correlate with happiness?
  
  <div align="center">
  
  <img width="681" alt="EconomicHealth vs Happiness correlation" src="https://user-images.githubusercontent.com/65078870/86192663-168a6800-bb18-11ea-8708-82530e2e6ab8.PNG">
  
  </div>
  
 
  <div align="center">
  
  <img width="687" alt="EconomicHealth vs Happiness Outliers" src="https://user-images.githubusercontent.com/65078870/86192733-3faaf880-bb18-11ea-988b-32d28f248158.PNG">
  
  </div>
  
   
   **_Observable Trends/Insights:_** 
  
  +   **GDP** had a strong positive relationship or correlation with Happiness Index while **Unemployment Rate** inversely showed a negative correlation. 
  
  +   We have identified outlier countries namely  **Costa Rica** and **Nicaragua**, for it demonstrated a relatively high Happiness Index scores even if its Log GDP was not outstanding. On the other hand, **Brazil** and **Spain**'s Happiness Index scores were also high in the midst of high Unemployment Rate.
   
  
  ----
  
  ### Summary of Correlations 
  
  #### What makes people happy and unhappy? 
  We looked at 23 variables (6 are from the World Happiness Report)
  
  <div align="center">
  
  <img width="725" alt="Correlations - All variables" src="https://user-images.githubusercontent.com/65078870/86067269-7d3d5200-ba42-11ea-80b7-c95f42f62555.PNG">
  
  </div>
  
  
   **_Observable Trends/Insights:_** 
   
   +  **Rev Tourism** and **Average Age** topped our positively correlated factors that impact Happinesss. 
   +  **Brain Drain** and **Security Index** showed the most negatively correlated factors that impact Happiness.  
  
  ----
  
  ### Outliers and Happiness Index Variables
  #### How do outliers perform on UN's Happiness Index variables?
  
  <div align="center">
  
  <img width="555" alt="Outliers-Perform Happiness Index Factors" src="https://user-images.githubusercontent.com/65078870/86343524-13ca6880-bc27-11ea-9291-5f273a47be08.PNG">
  
  </div>
  
  
   **_Observable Trends/Insights:_** 
   
   +  Outlier countries - *Costa Rica* , *Spain* , *Brazil* , and *Nicaragua* demonstrated that **Social Support** mattered most compared to the other factors that impact the Happiness Index within the UN's WHR.  
  
  
  
  ----
  
  ### Outliers and Other Factors
  #### How do outliers perform on other factors? 
  
  <div align="center">
  
  <img width="698" alt="Outliers-TopFactors vs Happiness and Unhappiness" src="https://user-images.githubusercontent.com/65078870/86342659-ec26d080-bc25-11ea-9d46-da5fc421fef2.PNG">
  
  </div>
  
  **_Observable Trends/Insights:_** 
  
  
  ----
  
  ### Canada and USA on Happiness
  #### How does Canada compare to US? 
  
  <div align="center">
  
  <img width="738" alt="Canada vs USA Perform" src="https://user-images.githubusercontent.com/65078870/86348315-82122980-bc2d-11ea-9adc-da45583d9e4c.PNG">
  
  </div>
  
  **_Observable Trends/Insights:_** 
  
  
  ----
  
  ### Happiness Over Time 
  ### How does happiness change over time?
  
  <div align="center">
  
  <img width="689" alt="Outliers and Canada Happiness over time" src="https://user-images.githubusercontent.com/65078870/86067929-0f922580-ba44-11ea-8755-2f0dfaeefdb8.PNG">
  
  </div>
  
  
  ---
  
  
  
  
  
  
  
  
  # Conclusion
  
  
  # Limitations
  
  
  

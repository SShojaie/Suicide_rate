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

Our primary dataset was obtained from the World Happiness Report (WHR) developed by UN's Sustainable Development Solutions Network. It's an annual publication that surveys the state of global happiness and ranks countries by how happy their citizens perceive themselves to be, which the report also correlates with various life factors. 

The group also searched for other factors that could potentially impact the measure of happiness. Those datasets were derived from different sources such as the Global Health Data Exchange (GHDx) by the University of Washington, The Global Economy, Central Intelligence Agency (CIA) Government and World Economic Forum websites. 

<div align="center">
  
<img width="454" alt="Sources Table" src="https://user-images.githubusercontent.com/65078870/86603006-75653c80-bf71-11ea-8f1b-f6388edb3ba0.PNG">

</div>

## Hypothesis

<div align="center">

> "A country's economic health by measure of GDP and Unemployment does not impact its people's happiness"

</div>

<div align="center">
  
> "Are richer nations happier?" 

</div>

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
  + Spain has the highest earnings from Tourism, while all other outlier countries underperform on this indicator. The average age of the outlier countries is low indicating that younger population perform better on happiness index and these factors are positively corelated to happiness index.
  
  + Brain drain is a challenge for these countries, maximum brain drain occurs in Nicaragua, affecting its happiness index. Security threat could be one of the major reasons for impacting the perception of happiness, therby brain drain and security threat negatively impact the happiness index.
  
  ----
  
  ### Canada and USA on Happiness
  #### How does Canada compare to US? 
  
  <div align="center">
  
  <img width="738" alt="Canada vs USA Perform" src="https://user-images.githubusercontent.com/65078870/86348315-82122980-bc2d-11ea-9adc-da45583d9e4c.PNG">
  
  </div>
  
  **_Observable Trends/Insights:_** 
  + Although Canada has a lower GDP compared to USA but it has higher happiness index due to the other factors like Social support, Healthy life expectancy, freedom, perception of corruption and generosity. This clearly demonstrates that GDP is not the most dominant factor in measuring a countries happiness index  
  
  ----
  
  ### Happiness Over Time 
  ### How does happiness change over time?
  
  <div align="center">
  
  <img width="689" alt="Outliers and Canada Happiness over time" src="https://user-images.githubusercontent.com/65078870/86067929-0f922580-ba44-11ea-8755-2f0dfaeefdb8.PNG">
  
  </div>
  
  
  ---
  
  
  
  
  
  
  
  
  # Conclusion
  
  
  # Limitations
  
  
  # Appendices
  
  
  Reference/Sources: 
+   https://ghdx.healthdata.org
+   https://www.theglobaleconomy.com
+   https://www.cia.gov/library/publications/the-world-factbook/rankorder/2177rank.html
+   https://www.weforum.org/agenda/2019/04/which-countries-get-the-most-sleep-and-how-much-do-we-really-need/
  

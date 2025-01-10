#exercise - Slides [1_Forecasting](1_Forecasting.pdf)

84 slides de bonheur
![](Pasted%20image%2020250106105418.png)
## Forecasting definition and motivation
#Forecasting is important as/for:
- The future is uncertain
- Uncertainties at the core of demand and supply
- Improving profitability, productivity, and customer service
- Controlling costs 
- Managing changes

**Planning** is crucial to navigate properly the different blocks of the SMO (Supply Market Operations).

 #Forecasting definition:
 - An attempt to determine in advance the most likely outcome of an uncertain variable
 - An objective estimate of future demand by projecting the past into the future
 - "“the business function that attempts to predict sales and use of products so they can be purchased or manufactured in appropriate quantities in advance.” APICS dictionary

Any 1% **improvement** on forecast visibility leads to:![](Pasted%20image%2020250106105813.png)
## How to build a forecasting model
A good #Forecasting-model is based on a framework of 5 blocs: #granularity, #temporality, #metrics, #process and #method.
### Granularity
For the #granularity 
![](Pasted%20image%2020250106110300.png)

### Temporality
For #temporality:
![](Pasted%20image%2020250106110346.png)

For example, when we have monthly orders and a lead time of 3 months, on which month should we focus for the forecast?
![](Pasted%20image%2020250106110751.png)
![](Pasted%20image%2020250106110742.png)
Indeed, the risk period is the lead time + a certain review period.

There are multiple levels of forecast:
![](Pasted%20image%2020250106112454.png)
Depending on the company, short-mid-long term forecast definition may vary.
### Metrics
#Metrics are useful to **track**, **measure** and **update** forecasts.

Often, the #Bias and the #Precision are studied.
- #Precision is the measure of the expected **average error**
- #Bias is the measure of the forecast **error spread**.
![](Pasted%20image%2020250106110617.png)
There are many measures for measuring the forecast error: #APE, #MAPE, #ME, #MAE, #RMSE 
![1_Forecasting](1_Forecasting.pdf#page=23)
### Process
The #process:
![](Pasted%20image%2020250106112829.png)

It is important for processes that the **data** is accurate. Because the **demand is not the same as the sales** for most of the times.

The reasons that may causes this difference are:
- Collaboration with clients
- Products cannibalization (a big order cannibalizes small orders)
- Sales Order Management system
- Track Out-of-Stocks
- Analyze Demand Drivers

In the data there can be mistakes, errors or exceptional demand (outliers) that will perturb the forecast.

Therefore, detection method for cleaning exists: **winsorization, error std and std**.
### Method
#method will be seen in the next section.

## Forecast techniques
![](Pasted%20image%2020250106111142.png)
The #forecasting techniques are divided in three classes:
- #qualitative techniques
- #quantitative techniques 
- And #ML (Machine Learning)

Note that #quantitative and #qualitative methods are complementary and **must be tested/combined** to produce an accurate and usable forecast.
### Qualitative techniques
#Qualitative methods are *based on intuition or judgmental evaluation*, workforce experience or on surveys. 

It is applicable for long and medium-term forecasts, even if there is insufficient history (for a new product or service for example).

In this type of clustering we need to **pay attention to**:
- Social pressure/Hierarchical/Political pressure 
- Budget pressure 
- Cognitive Bias $\to$ *Forecast should not be done by the users*
#### Delphi Models
1. Send questionnaires to experts 
2. Gather anonymous answers 
3. Send back the aggregated results to experts
4. Back to step 1 until agreement

**Advantages**:
- Capabilities when no patterns and relationships
- Easily and quickly assembled
**Disadvantages**:
- Lack of supporting evidence 
- Overconfidence 
- Possibility of over conformity of the individuals
- High cost of development and maintenance
### Quantitative techniques
#Quantitative methods apply for sizeable historical data (time series), clear and stable relationships and patterns in data for short/medium term forecast.

First an analysis can be made on the time series: trends, seasonality, cyclical and randomness. Therefore, decomposition methods exists (additive or multiplicative).
![](Pasted%20image%2020250106114258.png)
![1_Forecasting](1_Forecasting.pdf#page=46)
#### Time series forecasting models
#Time-series forecasting on models based on **pattern + noise**.

The simplest is the naive technique:
![](Pasted%20image%2020250106114533.png)
##### Simple moving average forecast
![](Pasted%20image%2020250106114430.png)

Another way to write this equation:![](Pasted%20image%2020250106115140.png)
##### Weighted moving average forecast
![](Pasted%20image%2020250106114443.png)
##### Exponential smoothing forecast
![](Pasted%20image%2020250106114453.png)
The choice of a value for $\alpha$ plays an important role in the exponential smoothing method. High values of  $\alpha$ give a larger weight to the most recent historical data and therefore allow us to follow rapidly the demand variations. On the other hand, lower values of $\alpha$ yield a forecasting method less dependent on the random fluctuation but, at the same time, cannot take quickly into account the most recent variations of the demand. In practice, the value of $\alpha$ is frequently chosen between 0.01 and 0.3. However, a larger value may be preferable if rapid demand changes are anticipated.
![](Pasted%20image%2020250106115512.png)

And if we are loco loco:![](Pasted%20image%2020250106115637.png)
#### Associative (Extrinsic) forecasting
##### Simple linear Regression forecast
![](Pasted%20image%2020250106115657.png)
##### Multiple regression forecast
Same as simple linear regression but with multiple explanatory variables.
![](Pasted%20image%2020250106115708.png)
### Parameter optimization
Parameters for the different models:
![](Pasted%20image%2020250106115756.png)

Parameters for splitting the dataset:
![](Pasted%20image%2020250106115833.png)
#### Underfitting vs Overfitting
![](Pasted%20image%2020250106134930.png)
#Underfitting
Some forecast models will not be able to properly predict or explain the reality. A model is **underfitted** if it does not explain reality properly enough.

The **causes** are:
- Model complexity is too low
- Lack of explanatory variables

**Solutions** may be to:
- Change the model for a more complex one
- Use more explanatory variables

#Overfitting
- Recognizing patterns from the noise (randomness) of the training set. 
- Re-apply these patterns in the future. 
- Good results on the training dataset. 
- Fail to make good predictions on the test set.
**Causes**:
- Model complexity is too high
- More explanatory variables

**Solutions**:
- Use less explanatory variables
- Use simpler model
- Use more data
- Don't fit on the test set
### Machine Learning #ML 
Brings a new version of the old school statistics:
![](Pasted%20image%2020250106135013.png)

#ML can be seen as a **black box**.

What is important in #ML is to know:
- Which data to feed the algorithm
- Which machine learning algorithm to use
- Which parameters to use

Before applying the #ML algos, it is **data cleaning**, because if you give garbage to the best cook, he will cook garbage lol:
1. Remove unwanted observations
2. Fix structural errors
3. Filter unwanted outliers
4. Handle missing data (dropping observations with missing values OR impute missing values based on other observations)
![1_Forecasting](1_Forecasting.pdf#page=78)

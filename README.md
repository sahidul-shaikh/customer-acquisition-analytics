## Bank Customer Acquisition Analysis for a Term Deposit Product

A Portuguese bank had conducted a telemarketing campaign for a term deposit product somewhere around late 2010. A term deposit is very similar to a fixed deposit, where we deposit money for a fixed period of time.  

Through the campaign, the bank had collected data about the prospects' demographics, other financial products they have purchased in the past (loans, deposits, etc.), the number of times they were called, etc. They also recorded the response data, i.e., whether the person had subscribed to the term deposit product, which is the target variable. 

The bank's marketing team wants to launch yet another telemarketing campaign for the same product. As an analyst at the bank, we want to answer the following questions using the past data:

- Which prospects are more likely to buy the product (i.e., to respond )?
- Which attributes determine the propensity to buy a term deposit?  
- Once we predict the likelihood of response, how many prospects should we target for telemarketing?
- By how much can we reduce the marketing cost using the model, and how many prospects will we acquire?

## Problem and Business Objective

- To reduce customer acquisition cost by targeting the ones who are likely to buy
- To improve the response rate, i.e., the fraction of prospects who respond to the campaign

## Data

- ***Customer data:*** Demographic data, data about other financial products like home loans, personal loans, etc.
 - ***Campaign data:*** Data about previous campaigns (number of previous calls, number of days since the last call was made, etc.)
- ***Macroeconomic data***
- ***Target variable:*** Response (Yes/No)

## Tasks

To solve the problem, we should build model without including the variable ‘duration’. Because the prospect data procured by the marketing team does not contain ‘duration’, since the call has not been made yet. This will help us understand the relationship of the other variables with the response.

Also, set the business objective to achieving 80% of total responders at the minimum possible cost. The total number of responders is the total number of prospects who responded, from the available data of about 45,000 prospects.

Based on this information, calculate the X in the top X%, i.e., how many prospects should be called to meet the business objective. 

## Checkpoints

The checkpoints for the assignment are as follows:

1. Perform data preparation and EDA.

2. Build a logistic regression model without using the variable 'duration'

  - Select variables using the usual methods
  - Sort the data points in decreasing order of the probability of response
  - Find the optimal probability cut-off and report the relevant evaluation metrics

3. Create a data frame with the variables prospect ID, actual response, predicted response, predicted probability of response, duration of the call in seconds and cost of the call

4. Find the number of top X% prospects we should target to meet the business objective
  - Report the average call duration for targeting the top X% prospects.

5. Create a lift chart

  - The x-axis should show the number of prospects contacted; the y-axis should show the ratio of the response rate using the model and the response rate without using the model

6. Determine the cost of acquisition for 80% of customers using the predictive model.

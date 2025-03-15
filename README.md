# Gasoline Price-Demand Analysis Using Linear, Log-Lin, Log-Log Models in R
This project analyzes the impact of gasoline prices on demand in Washington, DC, using Linear, Log-Lin, and Log-Log models. It compares model performance, interprets slope coefficients, and predicts demand at given price levels. The repository includes an R script for data processing, model fitting, and analysis. 

## Basic Information
**Names:** N M Emran Hussain  
**Email:** nmemranhussain2023@gmail.com  
**Date:** February 2025
**Model Version:** 1.0.0  
**License:** [MIT License](LICENSE)

## Intended Use
**Purpose:** Using models like Linear, Log-Lin, Log-Log we would like to predicts the impact of gasoline prices on demand in Washington, DC.  
**Intended Users:** Data Analysts, Data scientists, machine learning enthusiasts, educators.  
**Out-of-scope Uses:** The model is not intended for production use in any critical applications or real-time decision-making systems.

## Data Description

| **Variable Name**       | **Model Role**        | **Measurement Level**  | **Description**                                                    |
|-------------------------|-----------------------|------------------------|--------------------------------------------------------------------|
| Price	                  | Independent Variable	| Continuous	           | Average price of a gallon of gasoline (in dollars) on a given day  |
| Demand	                | Dependent Variable	  | Continuous	           | Average number of gallons of gasoline sold per station on that day |  

**Dataset Name:** AAA.dat  
**Number of Samples:** 42  
**Features Used:** 'Price'  
**Target Variable used:** 'Demand'  

## Model Details
### Architecture  
- This model card utilizes linear models such as **'Linear Regression, Log-Lin, Log-Log'**.

### Version of the Modeling Software: 
- **R:** 4.3.2
- **dplyr:** 1.1.4  

### Evaluation Metrics  
- **P-value:** Indicates statistical significance using 95% confidence level.
- **b-value:** Represents the magnitude and direction of **'slope'** of independent variable in a model.
- **Coefficient of multiple determination (R²)** - Indicates the strength of relationships between independent and dependent variables in **'sample'**. It is also denoted by CD.

## Quantitative Analysis

- Using a Linear Model, the interpretation of the **slope parameter (-1770.12)** means every one dollar in inncrease of price corresponding to an expected decease of 1770.12 gallons of gasoline in demand.
- Using a Log-Lin Model, the interpretation of the **slope parameter (-0.5096)** which dosn't fit the range of -0.1 to +0.1, So we can interpret the value of b1 in a 'formal way'. For every 1 dollar of inncrease in price corresponding to an expected **decrease of [100*{e^(-0.5096)}-1] or approximately 40% gallons of gasoline demand**.
- Using a Log-Log Model, the interpretation of the **slope parameter (-1.7757)** means if price **increases by 1% the demand of gallons of gasolines will be decreased by 1.7757%.**
- Among these three models **the best model for predicting** the relationship between 'price' and 'demand' is **the log-log model** because it has the **highest R-square** value of 0.9989 both in sample and population data. It means logarithm of price can explain the logarithm of demand in most efficient way.
- If the price of gasoline is $3.00 per gallon, the expected demand (in gallons) under a **Linear Model is 4356.463.**  
- If the price of gasoline is $3.00 per gallon, the expected demand (in gallons) under a **Log-Lin Model is 4425.604.**  
- If the price of gasoline is $3.00 per gallon, the expected demand (in gallons) under a **Log-Log Model is 4480.003.**   














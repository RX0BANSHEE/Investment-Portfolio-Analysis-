# Investment-Portfolio-Analysis-

I want to create a model to predict a stock long-term price that can generate some thoughtful insights to help me adjusting my investment portfolio.

Approach 
For the purpose of this project, there are 5 questions we want to ask:
1.	How to measure stock price in same level?
2.	How to compute each stock expected return?
3.	How to measure each stock volatility/ risk?
4.	How do we know which stock is profitable?
5.	How we know the portfolio we created is worth to investment.
So, to better generate the expected outcome from the project, 3 main steps we will walk through to answer the questions we listed: data gathering and processing, return and risk analysis via various plots, find suitable risk – return interval by using Monte Carlo Simulation. 

Methods
1. Searching data points 
To modify my project outcomes, the raw dataset which included historical price records from 01/01/2018 to 01/01/2021 about several famous company in the US, such as:
Apple Inc. (AAPL)
The Boeing Company (BA)
Citigroup Inc. (C)
Starbucks Corporation (SBUX)
International Business Machines Corporation (IBM)

2. Data Source Selection
According to the requirements of the previous data points, the data source we are looking for is not only reliable and free, but also has low timeliness requirements, and can be used for subsequent data processing and analysis through Jupyter Notebook.

At first, we planned to use Google's stock module, but found that the functions it provided were too simple, only one number could be seen, and even basic technical analysis charts could not be made to help you understand the market, which was only suitable for quick browsing.

Finally, we chose Yahoo Finance as the data source of our project. The important reason why we decided to use Yahoo Finance is that it is free. Compared with the paid information source, only one minute delay is needed to update the quotation, but it is enough for this project.

3. Stock normalization and overview analysis
Before we begin to analyze our stocks, we need to standardize our data so that we can compare their historical performance and further calculate the expected returns of these stocks. Therefore, we set the adjusted closing price of each stock at 1 on 2 January 2018. Any subsequent adjustments to the closing price are based on a relative conversion of the current share price, thus standardizing the share price.

4. Stock profitable ability and risk measurement analysis
After standardizing the daily price changes, we will assess the investment value of each stock on this basis. We split the value of our investments into two components, namely, volatility risk and profitability.


5. Portfolio Return Simulation  
Monte Carlo simulation, also known as statistical simulation, is a method to solve problems by generating appropriate random numbers and observing some data with specific properties or attributes. It provides approximate solutions for various mathematical problems by statistical sampling experiments on computers. This method is very effective for obtaining digital solutions for some problems that are too complicated to be analyzed and solved, and it is also suitable for problems with no probability and inherent probability structure.
Back to our project, we will execute 50000-time simulations and create a scatter plot to record each simulation generate expected return and standard deviation for five-stocks portfolio. The plot which shows below. 

Conclusion
All in all, according to the Monte Carlo Simulation Outcome and compare with the single stock performance like Apple (0.00175 return and 0.022), the 5-stock performance is more stable even though loss some return. We can say this portfolio make a good example to balance return and risk.



Packages used:

import numpy as np

import pandas as pd

import matplotlib.pyplot as plt


import seaborn as sns


import warnings

from datetime import datetime



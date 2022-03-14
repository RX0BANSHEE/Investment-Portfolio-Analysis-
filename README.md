# Investment-Portfolio-Analysis-

I want to create a model to predict a stock long-term price that can generate some thoughtful insights to help me adjusting my investment portfolio.

Methods
1. Searching data points 

2. Data Source Selection

3. Stock normalization and overview analysis

4. Stock profitable ability and risk measurement analysis

5. Portfolio Return Simulation  

Conclusion
All in all, according to the Monte Carlo Simulation Outcome and compare with the single stock performance like Apple (0.00175 return and 0.022), the 5-stock performance is more stable even though loss some return. We can say this portfolio make a good example to balance return and risk.



Packages used
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns; sns.set()
plt.style.use('seaborn-white')
import warnings
from datetime import datetime
warnings.filterwarnings("ignore")

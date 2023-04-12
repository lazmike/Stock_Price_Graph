# Stock_Price_Graph
#Tracks the closing prices of five stocks over the period 2016-2021

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Bank of America
BAC = pd.read_csv("BAC.csv",parse_dates=True,index_col='Date')
# JP Morgan
JPM = pd.read_csv("JPM.csv",parse_dates=True,index_col='Date')
# CitiGroup
C = pd.read_csv('C.csv',parse_dates=True,index_col='Date')
# HSBC
HSBC = pd.read_csv("HSBC.csv",parse_dates=True,index_col='Date')
#Royal Bank of Canada
RY = pd.read_csv("RY.csv",parse_dates=True,index_col='Date')

portfolio_list = [BAC,JPM,C,HSBC,RY]
portfolio_dict = {'BAC':BAC,'JPM':JPM,'C':C,'HSBC':HSBC,'RY':RY}

plt.figure(figsize = (10,4))
for entry in portfolio_dict:
    plt.plot(portfolio_dict[entry]['Adj Close'], label = entry)
plt.legend()

[BAC.csv](https://github.com/lazmike/Stock_Price_Graph/files/11209876/BAC.csv)
[C.csv](https://github.com/lazmike/Stock_Price_Graph/files/11209878/C.csv)
[HSBC.csv](https://github.com/lazmike/Stock_Price_Graph/files/11209879/HSBC.csv)
[JPM.csv](https://github.com/lazmike/Stock_Price_Graph/files/11209880/JPM.csv)
[RY.csv](https://github.com/lazmike/Stock_Price_Graph/files/11209881/RY.csv)
[WFC.csv](https://github.com/lazmike/Stock_Price_Graph/files/11209882/WFC.csv)

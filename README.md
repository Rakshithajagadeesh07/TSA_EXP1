# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
### Name : Rakshitha J
### Register Number : 212223240135
```
import pandas as pd
import matplotlib.pyplot as plt
file_path = 'silver.csv'  
data = pd.read_csv(file_path)
data.head()
data['Date'] = pd.to_datetime(data['Date'])
data.set_index('Date', inplace=True)
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['EURO'], label='Silver Price Today', color='blue')
plt.title('Silver Price Today Over Time')
plt.xlabel('Date')
plt.ylabel('EURO')
plt.grid(True)
plt.legend()
plt.show()
plt.figure(figsize=(10, 6))
plt.hist(data['EURO'], bins=20 , color='red',edgecolor='white')
plt.title('Silver Price Today Over Time')
plt.xlabel('Date')
plt.ylabel('EURO')
plt.show()
selected_columns = ['USD','GBP','EURO']
data[selected_columns].plot(kind='line', figsize=(15, 8))
plt.title('Line Plot for Selected Columns')
plt.xlabel('Date')
plt.ylabel('EURO')
plt.legend(loc='upper left')
plt.show()
```
# OUTPUT:

## Silver Price Today Over Time

![Silver price](https://github.com/user-attachments/assets/1e518922-7179-4953-ae69-4af63637aba6)

## Histogram

![Histogram](https://github.com/user-attachments/assets/de2ce7a2-a921-4bf5-bee6-9d7e505f6736)

## Line Plot

![Line plot](https://github.com/user-attachments/assets/5b23ab47-e1d6-4f2d-a1ee-0d3d3c9a92a9)

# RESULT:
Thus we have created the python code for plotting the time series of given data.

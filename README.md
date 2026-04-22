# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 22/04/2026
### Name: Karthikeyan C
### Reg.No: 212224040152

# AIM:
To Develop a python program to Plot a time series data.
# REQUIREMENTS:
1.Dataset-AirlinePassengers

2.Google Colab
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```py
from matplotlib import pyplot as plt
import pandas as pd
df = pd.read_csv('/mnt/data/AirPassengers.csv')
df['Month'] = pd.to_datetime(df['Month'])
df.set_index('Month', inplace=True)
print(df.dtypes)
df_resampled = df['#Passengers'].resample('D').interpolate(method='linear')
plt.figure(figsize=(12,6))
df_resampled.plot(kind='line', label='Interpolated Daily Passengers')
plt.title('Time Series Plot of Number of Passengers (Daily Interpolated)')
plt.xlabel('Day')
plt.ylabel('Number of Passengers')
plt.legend()
plt.grid(True)
plt.show()
```

# OUTPUT:
<img width="1005" height="547" alt="1a" src="https://github.com/user-attachments/assets/d88a34e7-ed9b-42cc-91a7-d3a646090621" />



# RESULT:
Thus we have created the python code for plotting the time series of given data.

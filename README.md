## Developed by : Divakar R
## Register number : 212222240026
## Date: 

# Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data for analysing the power consumption.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.
# PROGRAM:
```python
# Importing libraries
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd

# Reading the csv file 
df=pd.read_csv("powerconsumption.csv")
print(df)

# printing first five datasets values
df=pd.read_csv("powerconsumption.csv",parse_dates=["Datetime"],index_col="Datetime")
df.head()
 
# printing last five datasets values
df=pd.read_csv("powerconsumption.csv",parse_dates=["Datetime"],index_col="Datetime")
df.tail()

# labeling X and Y values
plt.xlabel("Datetime")
plt.ylabel("Temperature")
plt.title("power consumption")

# Use df.index to access the 'age' values since it's the index
plt.plot(df.index, df["Temperature"])
plt.show()

```

# OUTPUT:


![Screenshot 2024-08-21 214158](https://github.com/user-attachments/assets/68f25058-c71d-4d80-b41b-67c98d35d028)


# RESULT:
Thus we have created the python code for plotting the time series of given data.

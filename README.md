# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```py
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x, y, marker = 'o')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot')
plt.legend("Line1")
plt.show()
```
![image](https://github.com/user-attachments/assets/acb0a32f-e3ae-4a03-ad0d-5c2f37845252)
```py
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x1, y1, marker = 'o')
plt.plot(x2, y2, marker = 'o')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot')
plt.legend(["Line1", "Line2"])
plt.show()
```
![image](https://github.com/user-attachments/assets/8954c396-741a-4d9c-9c05-80e52973bea5)
```py
x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]

x = [1, 2, 3, 4, 5]
y1 = [10, 12, 14, 16, 18]
y2 = [5, 7, 9, 11, 13]
y3 = [2, 4, 6, 8, 10]
plt.plot(x, y1)
plt.plot(x, y2)
plt.plot(x, y3)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot')
plt.legend(["Line1", "Line2", "Line3"])
plt.fill_between(x, y1, y2, color='green', alpha=0.5)
plt.fill_between(x, y2, y3, color='red', alpha=0.5)
plt.show()
```
![image](https://github.com/user-attachments/assets/5f8c00f3-23ff-4fd9-9c71-d68fba7387bb)
```py
plt.plot(x_values, y_values)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot')
plt.show()
```
![image](https://github.com/user-attachments/assets/5f5cc082-1d96-42b3-9d0f-e929de55c6c8)
```py
from scipy.interpolate import make_interp_spline
x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])

spl = make_interp_spline(x, y)
x_new = np.linspace(x.min(), x.max(), 50)
y_new = spl(x_new)
plt.plot(x, y, 'o', label='data')
plt.plot(x_new, y_new, label = 'spline')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/d1639ab3-d654-4ac4-a913-4eeaca38c7fc)
```py
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]

c1 =['red', 'green']
c2 =['b', 'g']
plt.bar(names, values, color = c1)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Bar Plot')
plt.show()
```
![image](https://github.com/user-attachments/assets/3e6214df-de22-41f7-814b-07155594bf99)
```py
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/db08fe5a-a4e4-4631-82a6-d191ddad0d72)
```py
df = sns.load_dataset("tips")

avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()

plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/1444ad7f-c30e-4156-bca0-15797af34034)
```py
x_values = [0, 1, 2, 3, 4, 5]
y_values = [0, 1, 4, 9, 16, 25]

plt.figure()
plt.scatter(x_values, y_values, color="blue", label="Points")
plt.title("Simple Scatter Plot")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/f58c25e1-4aa4-4c49-9db6-69f4e59da85a)
```py
x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]

plt.figure()
plt.scatter(x, y, label="Stars", color="green", marker="*", s=30)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Custom Scatter Plot")
plt.legend()
plt.grid(True)
plt.show()
```
![image](https://github.com/user-attachments/assets/9e724eb3-82ac-4937-8bf0-60fe535baefc)
```py
activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']

plt.figure()
plt.pie(slices, labels=activities, colors=colors, startangle=90, autopct='%1.1f%%', shadow=True)
plt.title("Daily Activities")
plt.axis('equal')
plt.show()
```
![image](https://github.com/user-attachments/assets/48879a60-52fe-480f-b0c7-fc0f29560af4)

# Result:
 Data Visualization using matplot python library for the given data has performed Successfully.

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

x = [1,2,3,4,5]
y = [2,8,9,5,10]
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Line Plot")
plt.plot(x,y)
```
![image](https://github.com/user-attachments/assets/c36add07-b9ce-4f27-8623-5e5e11c6adcf)

```py
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x1,y1,label='line1')
plt.plot(x2,y2,label='line2')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph!')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/062fb7f0-e5f3-4078-9289-0c2be232e322)

```py
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='red',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='green',markersize=12)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Graph Customization')
plt.show()
```
![image](https://github.com/user-attachments/assets/b00228ee-398e-4e87-9c9e-c6b59c1b1252)

```py
yield_apples=[0.895,0.91,0.919,0.926,0.929,0.931]
plt.plot(yield_apples)
```
![image](https://github.com/user-attachments/assets/72d0f3c6-7775-4557-88d6-7288838f4a0f)

```py
years=[2010,2011,2012,2013,2014,2015]
yield_apples=[0.895,0.91,0.919,0.926,0.929,0.931]
plt.plot(years,yield_apples)
```
![image](https://github.com/user-attachments/assets/01313f8d-14fd-4821-8e5c-50807bf62424)

```py
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.926,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896, ]
plt.plot(years, apples)
plt.plot(years, oranges)
plt.xlabel('Year')
plt.ylabel('Yield (tons per hectare)')
plt.title('Crop Yields in Kanto')
plt.legend(['Apples','Oranges'])
plt.show()
```
![image](https://github.com/user-attachments/assets/004edf5d-0a24-4cf9-9588-b9f3a219dd5d)

```py
plt.figure(figsize=(12,6))
plt.plot(years,oranges,marker='o')
plt.title("Yield of Oranges (tons per hectare)");
```
![image](https://github.com/user-attachments/assets/d48d7f88-83d7-476e-8e10-438a9c5ba32c)

```py
x=np.arange(0,10)
y=np.arange(11,21)
x
```
![image](https://github.com/user-attachments/assets/a3a30e5f-709a-45d0-b9c2-86e402e08f6b)

```py
y
```
![image](https://github.com/user-attachments/assets/be20165e-566c-4b0b-8a5d-861edeb8043a)

```py
plt.scatter(x,y,c='r')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Graph in 2D')
```
![image](https://github.com/user-attachments/assets/537e7de5-3b62-4f95-9a43-277803ac5b7b)

```py
y=x*x
y
```
![image](https://github.com/user-attachments/assets/7b4256d4-7aa2-46f8-8300-733e67d55db7)

```py
plt.plot(x,y,'g*',linestyle='dashed',linewidth=2,markersize=12)
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('2d Diagram')
plt.legend(['y-values'])
```
![image](https://github.com/user-attachments/assets/6646aef1-80ef-48c2-8c62-695c02073edb)

```py
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("Sine Wave")
plt.plot(x,y)
plt.show()
```
![image](https://github.com/user-attachments/assets/d786f849-1799-4cb8-af28-e291ea0ba232)

```py
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
```
![image](https://github.com/user-attachments/assets/7a0a435b-0fc1-4e08-b91b-a9501870b3cf)

```py
 x=[1,2,3,4,5]
 y1=[10,12,14,16,18]
 y2=[5,7,9,11,13]
 y3=[2,4,6,8,10]
 plt.fill_between(x,y1,color='blue')
 plt.fill_between(x,y2,color='green')
 plt.plot(x,y1,color='red')
 plt.plot(x,y2,color='black')
 plt.legend(['y1','y2'])
 plt.show()
```
![image](https://github.com/user-attachments/assets/97f53c66-21c7-4d7b-ab43-382c8c23b542)

```py
 height=[10,24,36,40,5]
 names=['one','two','three','four','five']
 c1=['red','green']
 c2=['b','g']
 plt.bar(names,height,width=0.8,color=c1)
 plt.xlabel('x-axis')
 plt.ylabel('y-axis')
 plt.title('My bar chart!')
 plt.show()
```
![image](https://github.com/user-attachments/assets/8274577f-d45d-4fa3-8a6a-23cc5be8e9d1)

```py
 x=[2,8,10]
 y=[11,16,9]
 x2=[3,9,11]
 y2=[6,15,7]
 plt.bar(x,y,color='r')
 plt.bar(x2,y2,color='g')
 plt.title('Bar graph')
 plt.ylabel('Y axis')
 plt.xlabel('X axis')
 plt.show()
```
![image](https://github.com/user-attachments/assets/1f16707d-82cc-4466-a224-6b1911a0e6bc)

```py
 ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
 range=(0,100)
 bins=10
 plt.hist(ages,bins,range,color='green',histtype='bar',rwidth=0.8)
 plt.xlabel('age')
 plt.ylabel('No. of people')
 plt.title('My histogram')
 plt.show()
```
![image](https://github.com/user-attachments/assets/8b9b23dd-ddf2-4c4a-b070-662a81c43f28)

```py
 np.random.seed(0)
 data=np.random.normal(loc=0,scale=1,size=100)
 data
```
![image](https://github.com/user-attachments/assets/ec52c81f-ddf3-4f0f-9a5e-7ab60e308176)

```py
 fig,ax=plt.subplots()
 ax.boxplot(data)
 ax.set_xlabel('Data')
 ax.set_ylabel('Values')
 ax.set_title('Box Plot')
```
![image](https://github.com/user-attachments/assets/ea776263-740c-441c-86ce-a7d3a106e750)

```py
labels='Python','C++','Ruby','Java'
sizes=[215,130,245,210]
colors=['gold','yellowgreen','lightcoral','lightskyblue']
explode=(0,0.4,0,0.5)
plt.pie(sizes,explode=explode,labels=labels,colors=colors,autopct='%1.1f%%',shadow=True)
plt.axis('equal')
plt.show()
```
![image](https://github.com/user-attachments/assets/6bb52a97-852c-4dbb-8d33-0ed347bc2eb5)

```py
activities=['eat','sleep','work','play']
slices=[3,7,8,6]
colors=['r','y','g','b']
plt.pie(slices,labels=activities,colors=colors,startangle=90,shadow=True,explode=(0,0,0.1,0),radius=1.2,autopct='%1.1f%%')
plt.legend()
```
![image](https://github.com/user-attachments/assets/d6bfd85e-f4b8-4dfb-99bd-053e4c88a3e1)

# Result:
 Data Visualization using matplot python library for the given data has performed Successfully.

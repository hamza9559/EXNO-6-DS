# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 Include the necessary coding and corresponding screenshots

```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
df= sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/e849bc14-7726-4ace-b2f8-4be6bb3b92b1)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/user-attachments/assets/4bd25440-7b14-4a9e-95c0-864ef4839ab4)

```
import seaborn as sns
import matplotlib.pyplot as plt
# Load the tips dataset
tips = sns.load_dataset('tips')
#Calculate the average total bill and tip for each day of the week
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip =tips.groupby('day') ['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
#Set the labels and title
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![image](https://github.com/user-attachments/assets/ea9a1359-b4a7-4450-bdd3-fe1dfa2038a3)

```
avg_total_bill = tips.groupby('time') ['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom = avg_total_bill, label='Tip', width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/5b7d5cfb-de19-4e12-bde6-e740a9c444f7)

```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
#Set labels and title
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/a2ffc4b1-d121-43d2-afeb-2c625000bf47)

```
tips = sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/1ddbd3e8-fd87-472f-84ac-efe5cce67360)

```
import seaborn as sns
import matplotlib.pyplot as plt
sns.histplot(data=tips,x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
![image](https://github.com/user-attachments/assets/92df37c4-4559-4033-a432-ae8c69951be5)

```
import seaborn as sns
import pandas as pd
tips =sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/230384aa-6609-465b-ab52-e5117e704b4b)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "maroon", "edgecolor": "green"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/177b3bb4-e77e-4fdd-ba4d-b7a1ac76b00b)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set2", inner="quartile")
#Add labels and title
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/20d6b50a-1371-4645-b17e-ffe1d1d24ee6)

```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip,palette = 'Set1')
```
![image](https://github.com/user-attachments/assets/11d7a36b-1830-47a0-86db-e82309434030)

````
sns.set(style = 'whitegrid') 
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])

````
![image](https://github.com/user-attachments/assets/eac41153-8538-4934-a244-93565fcd08db)

```
import seaborn as sns 
# use to set style of background of plot
sns.set(style="whitegrid")
# loading data-set
tips = sns.load_dataset("tips")
sns.violinplot(x="tip", y="day", data=tip,palette='Set3')
```
![image](https://github.com/user-attachments/assets/cb64d5d7-5730-4873-b5ed-e37732455093)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/40d1e992-9c40-4b86-97c3-adfcf39e1c57)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/3769c675-ab2f-4c3b-b1eb-3b6ecb8bd5b1)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set1',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/e17a1974-f5e4-451c-bd83-9223380c2d33)

```
# Import necessary libraries
tips = sns.load_dataset("tips")
numeric_cols = tips.select_dtypes (include=np.number).columns
corr = tips [numeric_cols].corr()
sns.heatmap(corr, annot=True, cmap='plasma',linewidths=0.5)
```
![image](https://github.com/user-attachments/assets/a8de48a5-aec7-4332-bf36-fbfe96cb617b)


# Result:
HENCE, DATA VISUALIZATION USING SEABORN LIBRARY IS PERFORMED SUCCESSFULLY.

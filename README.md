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

## NAME : GOKUL S
## REG NO : 212224230075

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1192" height="216" alt="image" src="https://github.com/user-attachments/assets/283addbe-2f2b-4291-b70b-7a80b4ba00c7" />

## LINE PLOT
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="721" height="469" alt="image" src="https://github.com/user-attachments/assets/04eeef91-c1c9-4aa9-be5e-376f9118aa0a" />

## Multi Line Plot
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="663" height="474" alt="image" src="https://github.com/user-attachments/assets/d854af01-8fdd-42fd-a2ff-124dd7ca9597" />

## Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="810" height="514" alt="image" src="https://github.com/user-attachments/assets/f2f42cae-8351-4650-a01e-dab3ff9ec115" />

## Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="695" height="466" alt="image" src="https://github.com/user-attachments/assets/3c884979-41f7-4347-93a5-ab5cfc61afad" />

## Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="625" height="469" alt="image" src="https://github.com/user-attachments/assets/4083f74d-259d-48b0-99a5-b0189f5df8d3" />

## Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="705" height="466" alt="image" src="https://github.com/user-attachments/assets/e6177fbe-e35f-4c10-aae6-5013550fbab8" />

## Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="742" height="492" alt="image" src="https://github.com/user-attachments/assets/f849932a-a0ee-4a95-80fb-3bdccc01e71d" />

## Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="714" height="467" alt="image" src="https://github.com/user-attachments/assets/af74f315-7833-44e4-97cc-ee8955dfcbc1" />

## Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="877" height="493" alt="image" src="https://github.com/user-attachments/assets/68a8966b-c4b9-40fa-8aea-3e14819ac505" />

## Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="711" height="528" alt="image" src="https://github.com/user-attachments/assets/8c297da0-2d2a-472c-a8c1-e6525314ccfe" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

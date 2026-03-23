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
import pandas as pd import seaborn as sns import matplotlib.pyplot as plt df=pd.read_csv("titanic_dataset.csv") df.head()
<img width="949" height="162" alt="image" src="https://github.com/user-attachments/assets/b0e85f07-150f-4bef-b711-cf66244ed318" />


 x=[1,2,3,4,5] y=[3,6,2,7,1] sns.lineplot(x=x,y=y) plt.title('Line Plot')
 
<img width="821" height="655" alt="image" src="https://github.com/user-attachments/assets/14d93a24-772f-45da-a985-399e17c52425" />

x=[1,2,3,4,5] y1=[3,5,2,6,1] y2=[1,6,4,3,8] y3=[5,2,7,1,4] sns.lineplot(x=x,y=y1) sns.lineplot(x=x,y=y2) sns.lineplot(x=x,y=y3) plt.title('Multi Line Plot')
<img width="833" height="654" alt="image" src="https://github.com/user-attachments/assets/6a1508a3-fa6d-49c7-bde0-01ff82230e04" />

plt.figure(figsize=(8,5)) sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow') plt.title("Fare Of Passenger By Embarked Town")
<img width="954" height="653" alt="image" src="https://github.com/user-attachments/assets/66ee4a83-ec0c-4ca2-9b78-d6c5d33d5297" />


sns.scatterplot(x="Age", y="Fare", data=df) plt.title('Scatterplot of Age vs Fare') plt.show()
<img width="804" height="631" alt="image" src="https://github.com/user-attachments/assets/da755cd3-f455-4164-b7e3-6fabfb817f78" />

sns.kdeplot(data=df['Age'], shade=True) plt.title('Density Plot of Passenger Ages') plt.show()
<img width="900" height="688" alt="image" src="https://github.com/user-attachments/assets/e83fae69-836d-46eb-ac65-b536879d16fa" />

numeric_df = df.select_dtypes(include=['float64', 'int64']) corr_matrix = numeric_df.corr() sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') plt.title('Heatmap of Titanic Dataset') plt.show() 
<img width="842" height="687" alt="image" src="https://github.com/user-attachments/assets/659d6327-c0df-4cc7-86c5-2507291dff09" />


# Result:
 Include your result here

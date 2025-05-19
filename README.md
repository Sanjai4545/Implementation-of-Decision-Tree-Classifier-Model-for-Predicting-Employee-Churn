# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas
2.Import Decision tree classifier
3.Fit the data in the model
4.Find the accuracy score
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:T.SANJAI 
RegisterNumber:24900899
import pandas as pd
df=pd.read_csv("/content/Employee.csv")
print("data.head():")
df.head()


print("data.info()")
df.info()


print("data.isnull().sum()")
df.isnull().sum()


print("data value counts")
df["left"].value_counts()


from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
print("data.head() for Salary:")
df["salary"]=le.fit_transform(df["salary"])
df.head()


print("x.head():")
x=df[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()


y=df["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred


from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy

print("Data prediction")
dt.predict([[0.5,0.8,9,260,6,0,1,2]])


from sklearn.tree import plot_tree
import matplotlib.pyplot as plt
plt.figure(figsize=(10,10))
plot_tree(dt,filled=True,feature_names=x.columns,class_names=['salary' , 'left'])
plt.show() 
*/
```

## Output:
![image](https://github.com/user-attachments/assets/d2242694-84f1-4373-9225-407760b258e9)
![image](https://github.com/user-attachments/assets/9825ed32-4177-44ff-ba10-fb31d07c2db5)
![image](https://github.com/user-attachments/assets/a6bbb3b0-7024-4ace-9484-808d8c1001e2)
![image](https://github.com/user-attachments/assets/e53d2ffd-b640-4342-b717-0d251035f9b1)
![image](https://github.com/user-attachments/assets/438aec48-fd6c-4ded-8962-4da4bacff718)
![image](https://github.com/user-attachments/assets/53989d57-8b48-4578-8255-dc9fd08cce2f)
![IMG-20250519-WA0011 1](https://github.com/user-attachments/assets/75b71b1f-f275-4ade-b54d-812d2d1b42e9)
![IMG-20250519-WA0012 1](https://github.com/user-attachments/assets/877839f5-bfad-4c11-beb4-9790d729f5a3)
![IMG-20250519-WA0013 1](https://github.com/user-attachments/assets/55f41756-268b-449d-831d-3fbbe5fe5019)











## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.

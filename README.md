# Mini-Project
## AIM:
To predict and analyse the second hand car.
## MOTIVE:
The prices of new cars in the industry is fixed by the manufacturer with some additional costs incurred by the Government in the form of taxes. 
So, customers buying a new car can be assured of the money they invest to be worthy.
But due to the increased price of new cars and the incapability of customers to buy new cars due to the lack of funds, used cars sales are on a global increase . 
There is a need for a used car price prediction system to effectively determine the worthiness of the car using a variety of features. 
Even though there are websites that offers this service, their prediction method may not be the best. 
So we are just trying to predict the selling price with the available and quality of the required components of the car.
![Screenshot_20221129_093607](https://user-images.githubusercontent.com/94165380/204605556-3d1546ff-6e69-45d3-ad7f-f372f90a90e3.png)

## CODE:
```
NAME: VISHAL M.A
REG NO: 212222230177
```
```
import pandas as pd
import numpy as np
import seaborn as sns
d=pd.read_csv("Car details v3.csv")
d
d.head(5)
d.info()
d.isnull().sum()
d.shape

sns.boxplot(x="selling_price",data=d)

from scipy import stats
z=np.abs(stats.zscore(d['selling_price']))
d2=d[(z<0.5)]
d2
d2.shape
sns.boxplot(x='selling_price',data=d2)

sns.histplot(x='selling_price',data=d)

sns.scatterplot(d['torque'],d['selling_price'],hue=d['year'])

d.corr()
sns.heatmap(d.corr(),annot=True)

sns.violinplot(x="torque",y="selling_price",data=d)
```
## OUTPUT:

### HEAD
![Screenshot 2022-11-29 232237](https://user-images.githubusercontent.com/94165380/204606715-e61a0653-e452-42e4-98de-ed2c1fe0ca47.png)
### D.INFO
![image](https://user-images.githubusercontent.com/94165380/204606871-40a1eb9d-1600-498f-a83b-cf92b02bf5b1.png)
### D.ISNULL().SUM()
![image](https://user-images.githubusercontent.com/94165380/204607101-f92d0616-0824-4546-8e1d-915ec900ae60.png)
### D.SHAPE
![image](https://user-images.githubusercontent.com/94165380/204607197-df36f408-fbbd-46e6-bc04-e17e83d4b521.png)
### BOXPLOT WITH OUTLIERS
![image](https://user-images.githubusercontent.com/94165380/204607378-90dcffeb-4e8a-43db-94e9-cc6c71e4d8a5.png)
### BOXPLOT WITHOUT OUTLIERS
![image](https://user-images.githubusercontent.com/94165380/204607670-9504d7b7-c86d-4f17-be54-36e44bd61321.png)
### HISTOPLOT
![image](https://user-images.githubusercontent.com/94165380/204608061-8754f951-862c-40cc-993e-a1323bfb1da4.png)
### SCATTERPLOT
![image](https://user-images.githubusercontent.com/94165380/204608351-f1a37855-ce82-4580-9e5f-3b4d4d54a0fa.png)
### HEATMAP
![image](https://user-images.githubusercontent.com/94165380/204608603-3c8726b7-b95b-4d46-95b1-04ddf6336bae.png)
### VIOLIN PLOT
![image](https://user-images.githubusercontent.com/94165380/204608895-06105653-c5cb-4e97-be39-577d898fa246.png)

## RESULT:
Thus we have tried to predict and analyse second hand cars.


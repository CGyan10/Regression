# Regression

Regression model
#import pandas and matplotlib library

import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('Salary_Data.csv')
df

_____________________________________________________
#x= df.iloc[:,0]
#y= df.iloc[:,1]
#plt.scatter(x,y)
plt.scatter(df['YearsExperience'], df['Salary'])  # create scatter plot for predefinned labeled data

_______________________________________________________________________________________________________
#AIM - Build a linear regression model and find the best fit
# slope value
# intercept value
---------------------------------------------------
x = df.iloc[:, [0]]
y = df.iloc[:,1]
_______________________________--
from sklearn.linear_model import LinearRegression
model = LinearRegression() # call the leanear Regression method
model.fit(x,y) # Fit the model ( train)

----------------------------------------------------
model.coef_
----------------------
model.intercept_
---------------------
y = 9449.96232146x+25792.20019866871
------------------------------------------
y_pred =  model.predict(x)
plt.scatter(df['YearsExperience'], df['Salary'])
plt.plot(df['YearsExperience'],y_pred, c='r')
plt.show()
---------------------------------
model.predict([[2.5]])
---------------------------
9449.96*2.5+25792.2001


# pf-project-theory
[My repository](https://github.com/Abdullah998811/pf-project-theory)
import pandas as pd
df = pd.read_csv("C:\\Users\\786\\Desktop\\pf\\Student_Marks.csv")
# Data Cleaning  
df.head(3)
df.tail()
print(df)
df.info()
df.describe()
df.iloc[2] 
df.iloc[5] 
df['number_courses'].value_counts().plot(kind="bar")
df['number_courses'].value_counts().plot(kind="barh")
df['number_courses'].value_counts().plot(kind="area")
df['number_courses'].value_counts().plot(kind="box")
df['number_courses'].value_counts().plot(kind="density")
df['number_courses'].value_counts().plot(kind="pie")
df['number_courses'].value_counts().plot(kind="line")
df['number_courses'].value_counts().plot(kind="kde")
df.describe(include="all")
a = df['time_study']
print(a)
# Preprocessing
df.isnull()
df.sample(2)
# Slicing in Code
df[2:3]
df[3:2:5]
df[['number_courses']][1:3]
# std()-Standard Deviation
df['number_courses'].std()
# var() - Variance Calculation
df['number_courses'].var()
# Adding a new column 

df['col']=5
df
# Remove a column
df.drop(columns=['col'],inplace=True)
df
# Add a Row

a=pd.DataFrame({'number_courses':50,
                'Mark':'19.202',
                'time_study':'0.096'},
               index=[0])
a
df=pd.concat([a,df])
df
# Data Save

import pandas as pd
df = pd.read_csv("C:\\Users\\786\\Desktop\\pf\\Student_Marks.csv")
df
df.to_excel("newdata.xlsx", sheet_name="newsheet")

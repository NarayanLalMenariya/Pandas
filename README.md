# Pandas
Pandas Basics JBU
=====================================================
1. How to access jupyter notebook

---------------------------------------------
i.  Type jupyter notebook in command prompt
ii. open displayed html notepad in google chrome.
iii. click on new --> select python : it will open jupyter book

---------------------------------------------
2. How to read one csv file placed at desktop
---------------------------------------------
import pandas as pd
df = pd.read_csv("C:\Users\Sairampc\Desktop\FirstFilePandas.csv")
df  #printing dataframe

OUTPUT: 
Avg| Temp|	month| windSpeed
0	 | 29	 | April | 109
1	 | 30	 | may	 | 123
2	 | 34	 | June	 | 90
3	 | 27	 | July	 | 120
4	 | 26	 | aug	 | 123


=====================================================
3. How to create DataFrame using dictionary

---------------------------------------------

Create DataFrame using dictionary
whether_data = {
    'Avg Temp':[29,30,34,27,26],
    'Month':['April','May','June','July',"August"],
    'wind Speed':[109,123,90,120,123]
}
df2 = pd.DataFrame(whether_data)
df2

=====================================================
4. Achieve following operation on DataFrame df

a) print all columns
df.columns

----------------------------------------------
b) print individual columns
df.month #printing month column
df['Avg Temp'] #prinitn Avg Temp

----------------------------------------------
c) Print values from row 2 to 4
df[2:5]
----------------------------------------------
d) Get minimum , maximum & Avg Temp
df['Avg Temp'].min()
df['Avg Temp'].max()
df['Avg Temp'].mean()
----------------------------------------------
e) Print dataType of columns
type(df['Avg Temp'])
----------------------------------------------
f) Print Avg Temp and WindSpeed only
df[['Avg Temp','windSpeed']]
----------------------------------------------
g) Decribe wheter data
df.describe()
----------------------------------------------
h) Print temp using select command where temp is max
df[df['Avg Temp'] == df['Avg Temp'].max()]
----------------------------------------------

i) Print windSpeed where speed is >= 120
df[df.windSpeed >= 120]

#df.windSpeed[df[df.windSpeed >= 120]] //Not supported
# for indexing: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html
# pandas series operation : https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.html

----------------------------------------------
j) Print index range
df.index
----------------------------------------------
k) Instead of index = 0,1,2,3... change it to month
df.set_index('month',inplace=True)
----------------------------------------------
L) Get row of June month --> advantages of using set index
temp, speed = df.loc['June']
print(temp, speed)
df.shape

----------------------------------------------
M) Reset index again
df.reset_index(inplace=True)
df.shape

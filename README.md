# Pandas
Pandas Basics JBU
=====================================================
1. How to access jupyter notebook
---------------------------------------------
i.  Type jupyter notebook in command prompt
ii. open displayed html notepad in google chrome.
iii. click on new --> select python : it will open jupyter book
=====================================================
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
# Create DataFrame using dictionary
whether_data = {
    'Avg Temp':[29,30,34,27,26],
    'Month':['April','May','June','July',"August"],
    'wind Speed':[109,123,90,120,123]
}
df2 = pd.DataFrame(whether_data)
df2
=====================================================
4. Achieve following operation on DataFrame df


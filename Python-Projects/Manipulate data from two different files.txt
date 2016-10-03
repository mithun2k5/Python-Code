#Manipulte Data from two different files:
#Method 1

import pandas as pd
from pandas import DataFrame,Series

dframe1=pd.read_csv('Animal_Name.txt',delimiter = ' ')
dframe2=pd.read_csv('Speed.txt',delimiter = ' ')
dframe=pd.merge(dframe1,dframe2,on='Legs',how='left')
dframe.sort(['Speed'],ascending=0)

	Animal_Name	Legs	Speed
3	       Tiger	                     4	     4
2	         Cat	                     3	     3
0	    kangaroos	   2	     2
1	      Monkey	   2	     2

#Method 2

lst = []
for i in data:
    lst.append(i.split())
lst.remove(lst[0])

lst1 = []

for j in data1:
    lst1.append(j.split())
lst1.remove(lst1[0])

lst2 = []

for i in range(len(lst)):
    for j in range(len(lst1)):
        if lst[i][1] == lst1[j][0]:
            lst2.append((lst[i][0],lst1[j][1]))

for i in range(len(lst2)):
    for j in range(i+1,len(lst2)):
        if lst2[i][1] <= lst2[j][1]:
            temp = lst2[j]
            lst2[j] = lst2[i]
            lst2[i] = temp
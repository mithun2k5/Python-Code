import numpy as np

lst = [(-2,-4),(0,0),(10,15),(5,6),(7,8),(-10,-30)]
x,y = (5,5)
k = int(raw_input("Enter integer point::  "))
distance = []
length = len(lst)

for i in range(length):
    x1,y1 = lst[i]
    distance.append(np.sqrt((x1-x)**2 + (y1-y)**2))

for i in range(length):
    for j in range(length-1):
        if distance[j] > distance[j+1]:
            temp = distance[j]
            distance[j] = distance[j+1]
            distance[j+1] = temp
            
            new_temp = lst[j]
            lst[j] = lst[j+1]
            lst[j+1] =new_temp

for i in range(k):
    print lst[i]

#Output:
Enter integer point::  2
(5, 6)
(7, 8)
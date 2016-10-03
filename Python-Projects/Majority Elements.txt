#Majority Elements, if any element number is greater than n/2,print that element else print None:

lst =[3,3,4,2,4,4,2,4]

set_lst = list(set(lst))

half_length = len(lst)/2.0

dict1 = {}

for i in range(len(lst)):
    if lst[i] in dict1:
        dict1[lst[i]] = dict1[lst[i]] + 1
    
    else:
        dict1[lst[i]] = 1

max1 = 0
for i in dict1.keys():
    if dict1[i] > max1:
        max1 = i

if dict1[max1] > half_length:
    print max1
else:
    print 'None'
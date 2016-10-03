# Sort elements by frequency

from collections import OrderedDict

lst = [2,5,2,6,-1,9999999,5,8,8,8]
lst = sorted(lst)

dict1 = OrderedDict()

for i in range(len(lst)):
    
    if lst[i] in dict1:
        dict1[lst[i]] = dict1[lst[i]] + 1
    else:
        dict1[lst[i]] = 1
        
dict2 = sorted(dict1.items(),key = lambda x:x[1],reverse = True)

new_lst = []
for i in dict2:
    xx,yy = i
    for j in range(yy):
        new_lst.append(xx)
print new_lst

#Output:
[8, 8, 8, 2, 2, 5, 5, -1, 6, 9999999]
lst = [1,0,2,3,4,6,0,7,0,8]
lst1 = []
lst2 = []
length = len(lst)
for i in range(length):
    if lst[i] == 0:
        lst1.append(lst[i])
    else:
        lst2.append(lst[i])
length1 = len(lst1)
for i in range(length1):
    lst2.append(lst1[i])
lst2    
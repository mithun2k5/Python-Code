lst1 = [1,2,3,4,5]
lst2 = [3,4,5,6,7]
lst = []

for i in range(len(lst1)):
    for j in range(len(lst2)):
        if lst1[i] == lst2[j]:
            break
    else:
        lst.append(lst1[i])

for i in range(len(lst2)):
    for j in range(len(lst1)):
        if lst2[i] == lst1[j]:
            break
    else:
        lst.append(lst2[i])

#Output:
[1, 2, 6, 7]
lst = [1,2,3,4,5,6,7,8,9,10]
k=3
lst1 = []
for i in range(len(lst)):
    j= i + 1
    for j in range(len(lst)):
        if (lst[i]-lst[j]) == k:
            lst1.append((lst[i],lst[j]))
lst1

#Output:
[(4, 1), (5, 2), (6, 3), (7, 4), (8, 5), (9, 6), (10, 7)]
lst1 = ['C','D','E','F','G']
lst2 = [3,0,4,1,2]
lst3 = []

for i in range(len(lst1)):
    lst3.insert(lst2[i],lst1[i])
lst3

#Result:
['D', 'F', 'G', 'C', 'E']
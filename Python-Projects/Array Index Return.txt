lst = ["mithun","sachin","mithun","mithun"]
lst1 = list(set(lst))
lst2 = []
for i in range(len(lst1)):
    a = lst1[i]
    lst3 = [i for (y, i) in zip(lst, range(len(lst))) if a == y]
    lst2.append(lst3)
lst2

#Result:
[[0, 2, 3], [1]]  
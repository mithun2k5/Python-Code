#Flatten Nested List Iterator:

lst = [[1,2],2,[1,1]]
new_lst = []
for i in range(len(lst)):
    if type(lst[i]) == list:
        temp = lst[i]
        for j in range(len(temp)):
            new_lst.append(temp[j])
    else:
        new_lst.append(lst[i])
new_lst

Output:

[1, 2, 2, 1, 1]
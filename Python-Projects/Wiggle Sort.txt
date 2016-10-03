#Wiggle Sort

lst = [3,5,2,1,6,4]
#one possible output = [1,6,2,5,3,4]

for i in range(len(lst)-1):
    if i%2 == 0:
        if lst[i] > lst[i+1]:
            temp = lst[i]
            lst[i] = lst[i+1]
            lst[i+1] = temp
    else:
        if lst[i+1] > lst[i]:
            temp = lst[i+1]
            lst[i+1] = lst[i]
            lst[i] = temp
lst

#Output:

[3, 5, 1, 6, 2, 4]
lst = [1,2,3,4,5,6,7,8]
target = 8

for j in range(len(lst)):
    i = j + 1
    while (i<len(lst)-1):
        if ((lst[j]+lst[i]) == target):
            print "TRUE",(lst[j],lst[i])
            break
        i = i +1 

#Result:
TRUE (1, 7)
TRUE (2, 6)
TRUE (3, 5)
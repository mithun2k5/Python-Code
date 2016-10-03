#One procedure
s= '111'
lst = []
for i in range(len(s)):
    if i == 0:
        lst.append(s[i])
    elif i==1:
        lst.append(s[i-1]+s[i])
        lst.append(s[i]+s[i+1])
    else:
        lst.append(s[i-2]+s[i-1]+s[i])
lst=list(set(lst))
lst

#Output:
['1', '11', '111']

#Second Procedure:

lst = [3,4,7,1,2,9,8]
for i in range(len(lst)-4):
    for j in range(i+1,len(lst)-3):
        for k in range(j+1,len(lst)-2):
            for l in range(k+1,len(lst)-1):
                if lst[i]+lst[j] == lst[k] + lst[l]:
                    print (i,j,k,l)

#Output:
(0, 2, 3, 5)
(1, 2, 4, 5)

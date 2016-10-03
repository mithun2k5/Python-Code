lst1 = ['star','dog','car','rats','cra']

lst = []
while (len(lst1)>0):
    a = lst1[0]
    for j in range(1,len(lst1)):
        b = lst1[j]
        if sorted(lst1[0]) == sorted(lst1[j]):
            lst.append((a,b))
            lst1.remove(a)
            lst1.remove(b)
            break
    else:
        lst.append(lst1[0])
        lst1.remove(lst1[0])
lst

[('star', 'rats'), 'dog', ('car', 'cra')]
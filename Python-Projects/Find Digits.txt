#Find Digits

t = int(raw_input().strip())
for a0 in xrange(t):
    lst = []
    count = 0
    n = int(raw_input().strip())
    new = n
    while (new>0):
        lst.append(new%10)
        new = new/10
    for i in range (len(lst)):
        if lst[i]==0:
            continue
        elif n%lst[i] == 0:
            count = count + 1
    print count

#Output:
1
123456789
3
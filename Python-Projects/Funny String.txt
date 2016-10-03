num = input()

lst = []

for i in range(num):
    lst.append(raw_input(''))

for j in range(len(lst)):
    temp = lst[j]
    temp_rev = lst[j][::-1]
    k = 1
    for s in range(len(temp)-1):
        val = abs(ord(temp[k]) -ord(temp[s]))
        val_rev = abs(ord(temp_rev[k]) -ord(temp_rev[s]))
        if val != val_rev:
            print 'Not Funny'
            break
        k=k+1
    else:
        print 'Funny' 

#output

2
acxz
bcxz
Funny
Not Funny
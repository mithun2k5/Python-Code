#Fair Rations

N = int(raw_input().strip())
B = map(int,raw_input().strip().split(' '))

def  even_odd(num):
    if num%2==0:
        return 'EVEN'
    else:
        return 'ODD'

if even_odd(sum(B)) == 'ODD':
    print 'NO'

else:
    i = 0
    count = 0
    while (i<len(B)):
        if even_odd(B[i]) == 'ODD':
            B[i] = B[i] + 1
            B[i+1] = B[i+1] + 1
            i = i + 1
            count = count + 2
        elif even_odd(B[i]) == 'EVEN':
            i = i + 1
    print count

#Output

2
1 2
NO
#Find number of negative,positive and zeros in an array:

n = int(raw_input().strip())
arr = map(int,raw_input().strip().split(' '))

count_pos= 0.0
count_neg=0.0
count_zero=0.0
for i in range(len(arr)):
    if arr[i]>0:
        count_pos = count_pos + 1
    elif arr[i] == 0:
        count_zero = count_zero + 1
    elif arr[i]<0:
        count_neg = count_neg + 1
print '%.5f'%(count_pos/n)
print count_neg/n
print count_zero/n

#Output

6
-4 3 -9 0 4 1
0.50000
0.333333333333
0.166666666667
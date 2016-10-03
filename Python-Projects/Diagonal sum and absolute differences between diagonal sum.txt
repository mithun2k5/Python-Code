#Diagonal sum and absolute differences between diagonal sum
n = int(raw_input().strip())
a = []
rev_arr = []
for a_i in xrange(n):
    a_temp = map(int,raw_input().strip().split(' '))
    a.append(a_temp)
    a_temp1 = a_temp[::-1]
    rev_arr.append(a_temp1)

sum1 = 0
sum2 = 0

for i in range(len(a_temp)):
    for j in range(len(a_temp)):
        if i == j:
            sum1 = sum1 + a[i][j]


for i in range(len(a_temp1)):
    for j in range(len(a_temp1)):
        if i == j:
            sum2 = sum2 + rev_arr[i][j]
            
print abs(sum1-sum2)

3
11 2 4
4 5 6
10 8 -12
15
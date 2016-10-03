n = int(raw_input().strip())
A = map(int,raw_input().strip().split(' '))
lst = []

for i in range(n):
    tmp = A[i]
    j= i+1
    while (j<n):
        if tmp == A[j]:
            lst.append(abs(i-j))
        j = j + 1
if lst == []:
    print -1
else:
    print min(lst)

#Output:

5
1 2 3 4 10
-1
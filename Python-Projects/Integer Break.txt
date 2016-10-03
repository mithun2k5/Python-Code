#Integer Break:
#Using Recurrence formula: f(n) = max(f(n),max(i-j,f(i-j))*j) for 1 <= j < i

n = 5
lst = []
for i in range(n+1):
    lst.append(0)
lst[1] = 0
lst[2] = 1

for i in range(2,n+1):
    for j in range(1,i):
        lst[i] = max(lst[i],max(i-j,lst[i-j])*j)
lst

Output:

[0, 0, 1, 2, 4, 6]
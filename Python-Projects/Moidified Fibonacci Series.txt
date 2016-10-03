num = map(int,raw_input('').strip().split())

if num[0] == num[2]:
    print num[0]
    
elif num[1] == num[2]:
    print num[1]

else:
    num1 = []
    num1.append(num[0])
    num1.append(num[1])
    for i in range(1,num[2]):
        num1.append(num1[i-1] + num1[i]**2)
    print num1[i]

#Output:

0 1 6
27
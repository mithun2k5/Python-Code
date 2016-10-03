for i in range(2,20):
    for x in range(2,i):
        if i%x == 0:
            break
    else:
        print i," is prime"
#Output
2  is prime
3  is prime
5  is prime
7  is prime
11  is prime
13  is prime
17  is prime
19  is prime
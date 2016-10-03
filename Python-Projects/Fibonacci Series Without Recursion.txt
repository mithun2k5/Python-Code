def fib(num):
    a=1
    b=1
    print a
    for i in range(num-1):
        a,b = b,a+b
        print a
fib(5)

#Output:

1
1
2
3
5
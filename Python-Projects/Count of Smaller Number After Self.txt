#Count of Smaller Number After Self:

num = [5,2,6,1]

for i in range(len(num)):
    count = 0
    for j in range(i,len(num)):
        if num[i] > num[j]:
            count = count + 1
    print 'There are %s numbers to the left of %s'%(str(count),str(num[i]))   

#Output:

There are 2 numbers to the left of 5
There are 1 numbers to the left of 2
There are 1 numbers to the left of 6
There are 0 numbers to the left of 1
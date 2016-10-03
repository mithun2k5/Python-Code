def power_of_3(num):
    
    count = 0
    
    number = num
    
    if num%3 != 0:
        return 'This number can not be represented by the power of 3'
    
    while (num > 1):
        
        if num%3 == 0:
            count = count + 1
            num = num/3
        
        else:
            print 'This number can not be represented by the power of 3'
            break
    else:
        print '%s is equal to 3^%s'%(number,count)

#Output:

power_of_3(18)

This number can not be represented by the power of 3
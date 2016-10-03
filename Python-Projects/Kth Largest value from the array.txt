def K_largest_value(lst):
    length = len(lst)
    lst.sort()
    
    K = int(raw_input("Enter value::  "))
    if K>length:
        return "Out of Order."
    else:
        print "the value is:: ",lst[length-1-K]
        
#Output:
K_largest_value([4,10,5,4,3])
Enter value::  0
the value is::  10
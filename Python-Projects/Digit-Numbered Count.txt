def numcount():
    
    lst=[1,2,4,10,-30,456]
    count_single=0
    count_double=0
    count_triple=0
    for num in lst:
        if abs(num) < 10:
            count_single += 1
        elif abs(num) >= 10 and abs(num) < 100:
            count_double += 1
        elif abs(num) >= 100 and abs(num) < 1000:
            count_triple += 1
    print "single digits: ",count_single, "\n double digits: ",count_double, "\n triple digits: ",count_triple

#Output
numcount()

single digits:  3 
 double digits:  2 
 triple digits:  1
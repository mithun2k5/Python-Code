def hello(lst):
    length= len(lst)
    i = 0
    j = 0
    for x in lst:
        i = i + 1
        j = j + 1
        print "\n"
        print x,
        while (j<length):
            print "+",lst[j],
            j = j + 1
        j = i

#Output
hello(['x','y','z','w'])

x + y + z + w 

y + z + w 

z + w 

w
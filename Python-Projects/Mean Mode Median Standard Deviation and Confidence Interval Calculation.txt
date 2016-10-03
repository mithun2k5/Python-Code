import math
import collections
num_samples = input()
x = raw_input()
lst = map(int,x.split())
lst1 = sorted(lst)

### Mean
sum1 = 0.0
for i in range(len(lst1)):
    sum1 = sum1 + lst1[i]
mean = sum1/num_samples
print '%.1f' %(mean)

###Median
def odd_even(num):
    
    if num%2 == 0:
        return 'EVEN'
    else:
        return 'ODD'
    
if odd_even(num_samples) == 'ODD':
    median = lst1[num_samples/2]
    print '%.1f' %(median)
else:
    median = (float(lst1[num_samples/2]) + lst1[num_samples/2-1])/2
    print '%.1f' %(median)

####Mode
if lst1 == list(set(lst1)):
    mode = lst1[0]
    print mode
else:
    new_lst = list(set(lst1))
    dc = dict(collections.Counter(lst1))
    maximum = 0.0
    for i in new_lst:
        if dc[i]> maximum:
            maximum = dc[i]
    
    lst2 = []

    for i in new_lst:
        if dc[i] == maximum:
            lst2.append(i)
    lst3 = sorted(lst2)
    print lst3[0]
        


##Standard Deviation
temp = 0.0
for i in range(len(lst1)):
    temp = temp + (mean-lst1[i])**2
    
sd = math.sqrt(temp/num_samples)
print '%.1f' %(sd)

###Confidence interval of the mean:

val1 = mean - 1.96*(sd/math.sqrt(num_samples))
val2 = mean + 1.96*(sd/math.sqrt(num_samples))


print '{0:0.1f} {1:0.1f}'.format(val1, val2)

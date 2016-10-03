lst =[1,5,10,100]
lst5 = []
length=len(lst)
for i in range(length-1):
    sum1=lst[i]
    j=i
    for i in range(j,length-1):
        lst5.append(sum1+lst[i+1])
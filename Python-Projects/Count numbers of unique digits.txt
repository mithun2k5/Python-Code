#Count numbers of unique digits 0<=x<10^n

def count_unique_digits(num):
    num_range = pow(10,num)
    count = 0 
    for i in range(0,num_range):
        if i < 10:
            count = count + 1
        else:
            new_i = str(i)
            for j in range(len(new_i)-1):
                a = new_i[j]
                for k in range(j+1,len(new_i)):
                    if a != new_i[k]:
                        count = count + 1
    return count

count_unique_digits(2)
91


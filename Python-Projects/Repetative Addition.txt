#Repetative Addition

def add(num):
    new_num = 0
    for i in range(len(str(num))):
        new_num = new_num + num%10
        num = num/10
    return new_num

#Another Solution:

def repetative_add(num):
    if num < 10:
        return num
    else:

            while (len(str(num)) > 1) :
                new_num = 0
                for i in range(len(str(num))):
                    new_num = new_num + num%10
                    num = num/10
                num = new_num

    return new_num

#Output
repetative_add(9)
9
#Number of 1 bits in a number:
def one_bit_count(num):
    lst = []
    while (num/2 != 0):
        a = num % 2
        lst.append(a)
        num = num/2
    if num == 0 or num == 1:
        lst.append(num)
    lst = lst[::-1]
    
    count = 0
    for i in range(len(lst)):
        if lst[i] == 1:
            count = count + 1
    return count

#Output
one_bit_count(5)
2

def one_bit_count_extended(num):
    new_list = []
    for number in range(1,num + 1):
        lst = []
        while (number/2 != 0):
            a = number % 2
            lst.append(a)
            number = number/2
        if number == 0 or number == 1:
            lst.append(number)
        lst = lst[::-1]
        count = 0
        for i in range(len(lst)):
            if lst[i] == 1:
                count = count + 1
        new_list.append(count)
    return new_list

#Output:

one_bit_count_extended(5)

[1, 1, 2, 1, 2]
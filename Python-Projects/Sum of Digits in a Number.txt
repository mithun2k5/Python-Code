#Recursion Method:
def sum_digit(num):
    if num<10:
        return num
    else:
        return (num%10) + sum_digit(num/10)

#Normal Method:
def sum_digit1(num):
    a = 0
    while (num>10):
        a = a + num%10
        num=num/10
    return num + a    
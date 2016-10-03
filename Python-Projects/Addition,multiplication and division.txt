#Addition without using Arithmatic Operator:

def addition(a,b):
    while (b != 0):
        carry = a & b
        a = a^b
        b = carry << 1 #Left shift by 1 bit
    return a

#Multiplication without using multiplication operator
def multiplication(a,b):
    if b ==0:
        return 0
    else:
        return a + multiplication(a,b-1)


#Division without using division operator
def division(a,b):
    if b>a:
        return 0
    count = 0
    while (a>=b):
        a = a-b
        count = count + 1
    return count


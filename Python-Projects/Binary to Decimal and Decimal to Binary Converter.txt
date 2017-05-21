## Decimal to binary converter

decimal = int(input("Give Decimal Input: "))

def binary_converter(decimal):
    value = ""
    while (decimal > 1):
        value = value + str(decimal % 2)
        decimal = int(decimal/2)
    if decimal == 0:
        value = value + str(decimal)
    elif decimal == 1:
        value = value + str(decimal)
    new_value = value[::-1]
    value1 = "Binary value is:: " + new_value
    return value1

## Output
decimal = int(input("Give Decimal Input: "))
2
a=binary_converter(decimal)
print(a)
Binary value is:: 10

## Binary to decimal converter

binary = input("Give Binary Input: ")

def decimal_converter(binary):
    if len(binary) == 1:
        return int(binary)
    else:
        value = ""
        str_value = " ".join(binary)
        new_value = str_value.split()
        length=len(new_value)
        value=0
        i=0
        while (length>0):
            value = value + (int(new_value[i])*pow(2,length-1))
            i = i + 1
            length = length -1
    value = "Decimal valus is :: " + str(value)
    return value

## Output
binary = input("Give Binary Input: ")
1000
b=decimal_converter(binary)
print(b)
Decimal valus is:: 8

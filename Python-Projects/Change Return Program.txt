#Change Return Program

def change_return_program():
    cost = round(float(raw_input("Enter your cost(in dollar):: ")),2)
    money = round(float(raw_input("Enter your money(in dollar):: ")),2)
    
    return_amount = money - cost
    return_amount1 = return_amount
    penny = .01
    nickel = .05
    dime = .1
    quarter = 0.25
    dollar = 1.0
    dollar_number = 0
    quarter_number = 0
    dime_number = 0
    nickel_number = 0
    penny_number = 0
    if (return_amount >= dollar):
        dollar_number = int(return_amount)/1
        return_amount = return_amount%1
    if (return_amount >= 0.25):       
        quarter_number = int(return_amount/0.25)
        return_amount = round(return_amount - (0.25*quarter_number),2)
    if (return_amount >= 0.10 ):
        dime_number = int(return_amount/0.1)
        return_amount = round(return_amount - (0.1*dime_number),2)
    if (return_amount >= 0.05):
        nickel_number = int(return_amount/0.05)
        return_amount = round(return_amount - (0.05*nickel_number),2)
    if (return_amount >= 0.01):
        penny_number = int(return_amount/0.01)
       
    print "\n"
    print "Change Return Amount:: " + str(return_amount1) + " dollar"
    print "Number of Dollar:: ",dollar_number
    print "Number of Quarter:: ",quarter_number
    print "Number of Dime:: ",dime_number
    print "Number of Nickel:: ",nickel_number
    print "Number of Penny:: ",penny_number

#Output:

Enter your cost(in dollar):: 100
Enter your money(in dollar):: 149.9


Change Return Amount:: 49.9 dollar
Number of Dollar::  49
Number of Quarter::  3
Number of Dime::  1
Number of Nickel::  1
Number of Penny::  0
#Coin Flip Simulation:
import random
def coin_flip():
    head = 0
    tail = 0
    turn = int(raw_input("How many times want to flip the coin:: "))
    for i in range(1,turn+1):
        if random.randint(0,1) == 0:
            head = head + 1
        else:
            tail = tail + 1
    print "\n"
    print "Number of head:: ",head
    print "Number of tail:: ",tail

#output:

coin_flip()

How many times want to flip the coin:: 10


Number of head::  4
Number of tail::  6
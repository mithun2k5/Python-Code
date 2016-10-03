#Guess the Number

import random

num = random.randint(1,10)

trail = 3

for i in range(trail):
    guess_number = int(raw_input('Give number:: '))
    if guess_number == num:
        print 'You won!!! game over'
        break
    
    else:
        if guess_number > num:
            print 'Lower'
        else:
            print 'Higher'
            
        print 'Turn Left:: ',(3-(i+1))
        if i == 2:
            print 'You Lose, game over'

#Output:

3
Give number:: 8
Lower
Turn Left::  2
Give number:: 1
Higher
Turn Left::  1
Give number:: 5
Lower
Turn Left::  0
You Lose, game over
# template for "Guess the number" mini-project
# input will come from buttons and an input field
# all output for the game will be printed in the console
import simplegui
import math
import random

secret_number=0
counter=7
low=0
high=100

# helper function to start and restart the game
    

def new_game(new_low,new_high,new_counter):
    # initialize global variables used in your code here
    global secret_number,low,high,counter
    low=new_low
    high=new_high
    counter=new_counter
    secret_number=random.randrange(low,high)
    print "\nNew game.Range is from",low,"to",high
    print "Number of remaining guesses is",counter
    
# define event handlers for control panel
def range100():
    # button that changes the range to [0,100) and starts a new game 
    new_game(0,100,7)
        
def range1000():
    # button that changes the range to [0,1000) and starts a new game     
    new_game(0,1000,10)
    
    
def input_guess(guess):
    # main game logic goes here	
    global secret_number,counter,low,high
    guess=int(guess)
    print ""
    print "Guess was",guess
    counter=counter-1
    print "Number of remaining guesses is",counter
    if (counter>0):
        if (secret_number-guess)>0:
            print "Higher!"
        elif (secret_number-guess)<0:
            print "Lower!"
        elif (secret_number-guess)==0:
            print "Correct!"
            if (high==100):
                counter=7
                new_game(low,high,counter)
            else:
                counter=10
                new_game(low,high,counter)
    elif (counter==0):
        if (secret_number-guess)==0:
            print "Correct!"
        else:    
            print "Out of guesses"
            if (high==100):
                counter=7
                new_game(low,high,counter)
            else:
                counter=10
                new_game(low,high,counter)
    
# create frame
frame = simplegui.create_frame("Guess the number",300,300)

# register event handlers for control elements and start frame
frame.add_button("Range is [0,100]",range100,200)
frame.add_button("Range is [0,1000]",range1000,200)
frame.add_input("Enter a guess",input_guess,100)
frame.start()

# call new_game 
new_game(low,high,counter)


# always remember to check your completed program against the grading rubric

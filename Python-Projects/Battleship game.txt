#Battleship Game

#Creating Empty 5X5 board
board = []

for i in range(5):
    board.append(['O']*5)

#Print Board 
def board_condition(board):
    for i in board:
        print " ".join(i)

#Random selection of ship position in the board:
import random
row_random_choice = random.randint(0,4)
column_random_choice = random.randint(0,4)
#print row_random_choice
#print column_random_choice

#5 choice condition:
for choice in range(5):

#Player choice of co-ordinate:
    row_choice = int(raw_input("Row Input: "))
    column_choice = int(raw_input("Column Input: "))

#Game Condition
    if (row_choice == row_random_choice and column_choice == column_random_choice):
        print "Player Won!!"
        print "Choice Left: ",(5-(choice+1))
        break
    else:
        if (row_choice > 4 or row_choice <0 or column_choice > 4 or column_choice < 0):
            print "Wrong choice of co-ordinate !!"
        elif (board[row_choice][column_choice] == "X"):
            print "Already guessed!!"
        else:
            board[row_choice][column_choice] = "X"
        print "You missed your target"
        print "Choice Left: ",(5-(choice+1))
        if choice == 4:
            print "You lose!!"
            print "Game Over!!"
        board_condition(board)
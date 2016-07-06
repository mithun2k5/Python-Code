#Programing Structure:
import simplegui
import random
#Global variables(state)
message="Hello World"
position=[50,75]
x=0
y=0

#Helper Functions
#Classes

#Define event and draw Handlers
def input():
    global message
    message="Well Done!"

    
def input_handler(txt):
    global message
    message=txt
    
def draw(canvas):
    global message
    canvas.draw_text(message,position,20,"yellow")

def tick():
    global message,x,y,position
    x=random.randrange(0,200)
    y=random.randrange(0,200)
    position[0]=x
    position[1]=y

#Create a frame and/or canvas
frame=simplegui.create_frame("Hello",200,200)
frame.add_input("Add Text",input_handler,100)
frame.set_draw_handler(draw)
timer=simplegui.create_timer(1000,tick)
#Register event and draw handlers
frame.add_button("Click me",input,100)
#Start frame and timer
frame.start()
timer.start()



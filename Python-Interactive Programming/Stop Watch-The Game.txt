# template for "Stopwatch: The Game"
import simplegui 

# define global variables
counter=0
mins=0
secs=0
x=0
y=0
p=1

# define helper function format that converts time
# in tenths of seconds into formatted string A:BC.D
def format(t):
    global counter,mins,secs
    t=counter
    if (t==10):
        secs=secs+1
        counter=0
    elif (secs==60):
        mins=mins+1
        secs=0
    
# define event handlers for buttons; "Start", "Stop", "Reset"

#Start button-event handler

def button_start():
    global secs,x,y,counter,p
    p=0
    timer.start()

#Stop button-event handler    

def button_stop():
    global secs,x,y,counter,p
    if (p==0):
        if counter==0:
            p=p+1
            x=x+1
            y=y+1
            timer.stop() 
        else:
            p=p+1
            y=y+1
            timer.stop()  
    
#Reset button-event handler   
    
def button_reset():
    global counter,secs,mins,x,y,p
    counter=0
    secs=0
    mins=0
    x=0
    y=0
    p=1
    timer.stop()

    
# define event handler for timer with 0.1 sec interval
def tick():
    global counter
    counter=counter+1

# define draw handler
def draw(canvas):
    global counter,mins,secs,x,y
    format(counter)
    canvas.draw_text(str(x)+"/"+str(y),[130,30],30,"Yellow")
    if (secs<10):
        canvas.draw_text(str(mins)+":"+"0"+str(secs)+"."+str(counter),[50,100],40,"White")
    else:
        canvas.draw_text(str(mins)+":"+str(secs)+"."+str(counter),[50,100],40,"White")

# create frame
frame=simplegui.create_frame("Stopwatch:The Game",200,200)

# register event handlers
timer=simplegui.create_timer(100,tick)
button1=frame.add_button("Start timer",button_start,100)
button2=frame.add_button("Stop timer",button_stop,100)
button3=frame.add_button("Reset timer",button_reset,100)
frame.set_draw_handler(draw)
# start frame
frame.start()

# Please remember to review the grading rubric

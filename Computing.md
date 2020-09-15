#The following is for everybody to propose changes. Feel free to do one. Not all.
**Number one**

from microbit import *
import music:

tune = ["D4:2","D4:2","D5:4","A4:6","G#:4","G:3","F:3","D:2","F:2","G:2","C4:2","C","D5:4",
       "A4:6","G#:4","G:3","F:3","D:2","F:2","G:2","B3:2","B","D5:4","A4:6","G#:4","G:3",
        "F:3","D:2","F:2","G:2","A#3:2","A#","D5:4","A4:6","G#:4","G:3","F:3","D:2","F:2",
        "G:2",]

music.play(play,loop = True)

**Number 2**

from microbit import *
import munsico
situps = 0
timer = 0
waiting = False
#1 minute per sitting
display.scroll("Press button A to start.", wait = False, loop = True)
while True:
  #situp counter
  if button_b.was_pressed():
    situps = situps + 1
    display.show(Image.TRIANGLE)
    sleep(100)
    display.clear()
  if waiting == True:
    timer = timer + 1
    sleep(1000)
  #timer
  if timer > 59:
    display.clear()
    music.play(music.POWER_UP, wait = False)
    display.scroll("You completed " + str(situps) + "!")
    display.clear()
    timer = 0
    situps = 0
    waiting = False
  else:
    #start button
    if button_a.was_pressed():
      display.scroll('3, 2, 1, Go!')
      waiting = True
     
 **Number 3**
 Going strong yeah
 
from microbit import *
while True:
  if button_a.is_pressed:
    start = running_time
  if button_b.is_pressed():
    end = running_time()
    duration = end-start
    final = duration/60000
    display.scroll(str(final))
    display.scroll('min')
    if final < 15.2:
      display.show(Image.HAPPY)
 
**Number 4**
from microbit import *
display.show(Image.Tiger):
sleep(200
display.clear)
**Number 5**
from microbit import *
while True:
  if button_a.is_pressed():
    display.show(Image.HAPPY)
  else:
    display.show(Image.COW)



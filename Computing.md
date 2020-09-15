#The following is for everybody to propose changes. Feel free to do one. Not all.</br>
**Number one**</br>

from microbit import *</br>
import music</br>

tune = ["D4:2","D4:2","D5:4","A4:6","G#:4","G:3","F:3","D:2","F:2","G:2","C4:2","C","D5:4",</br>
       "A4:6","G#:4","G:3","F:3","D:2","F:2","G:2","B3:2","B","D5:4","A4:6","G#:4","G:3",</br>
        "F:3","D:2","F:2","G:2","A#3:2","A#","D5:4","A4:6","G#:4","G:3","F:3","D:2","F:2",</br>
        "G:2",]

music.play(tune,loop = True)</br>

**Number 2**</br>

from microbit import *</br>
import music</br>
situps = 0</br>
timer = 0</br>
waiting = False</br>
#1 minute per sitting</br>
display.scroll("Press button A to start.", wait = False, loop = True)</br>
while True:</br>
  #situp counter</br>
  if button_b.was_pressed():</br>
    situps = situps + 1</br>
    display.show(Image.TRIANGLE)</br>
    sleep(100)</br>
    display.clear()</br>
  if waiting == True:</br>
    timer = timer + 1</br>
    sleep(1000)</br>
  #timer</br>
  if timer > 59:</br>
    display.clear()</br>
    music.play(music.POWER_UP, wait = False)</br>
    display.scroll("You completed " + str(situps) + "!")</br>
    display.clear()</br>
    timer = 0</br>
    situps = 0</br>
    waiting = False</br>
  else:</br>
    #start button</br>
    if button_a.was_pressed():</br>
      display.scroll('3, 2, 1, Go!')</br>
      waiting = True</br>
     
 **Number 3**</br>
 Going strong yeah</br>
 
from microbit import *</br>
while True:</br>
  if button_a.is_pressed:</br>
    start = running_time</br>
  if button_b.is_pressed():</br>
    end = running_time()</br>
    duration = end-start</br>
    final = duration/60000</br>
    display.scroll(str(final))</br>
    display.scroll('min')</br>
    if final < 15.2:</br>
      display.show(Image.HAPPY)</br>
 
**Number 4**</br>
from microbit import *</br>
display.show(Image.Tiger)</br>
sleep(200)</br>
display.clear</br>
**Number 5**</br>
from microbit import *</br>
while True:</br>
  if button_a.is_pressed():</br>
    display.show(Image.HAPPY)</br>
  else:</br>
    display.show(Image.COW)</br>



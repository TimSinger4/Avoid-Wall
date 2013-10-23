Avoid-Wall
==========
## Fardad Hajirostami / Tim Singer
## B1
## realwaffle@gatech.edu / timsinger4@gatech.edu
## We worked on the homework assignment alone, using only this semester's course materials.

from Myro import *
init("COM8")

setIRPower(140)
def avoidWalls():
    start = currentTime()
    timer = currentTime() - start
    while timer < 60:
        timer = currentTime() - start
        if getIR("left") == 0:
            turnLeft(1,.5) and backward(1,.5)
        else:
            backward(1)
    if timer >= 60:
        print("Done Avoiding!")
        turnLeft(1,1) and backward(1,1)
        turnRight(1,1) and forward(1,1)
        beep(.5,1000)
        beep(.5,1500)
        beep(.5,1000)
        beep(.5,1500)

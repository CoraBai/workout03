##Getting Started with rolling an object
Yitong Bai
2018-11-24
Object Rolling
The package "roller" is a minimalistic simulation of rolling an object with different sides and probability a given number of times, and to visualize the relative frequencies in graphs.

###Creating a device
The first step is to create a "device" object with the function device():

defaultdevice <- device()
defaultdevice


By default, device() creates a fair device with standard sides 1, representing head and 2, representing tail and with probability values for each side of 0.5. This object is similiar to a coin.

Now we can change the parameters from default to sides and prob: make sure the sides and probability satisfy the respective requirements (ie: length sides should be larger than 1)

loaded <- device(sides = c(1, 2), prob = c(0.8, 0.2))
loaded


###Rolling a device
Once you have defined a "device" object, you can use the function roll() to roll the device a given number of times. The output will be an object of class "rolls"

roll100 <- roll(defaultdevice, times = 100)
roll100


The summary.rolls() function gives you a table of frequencies:

summary.rolls(roll100)


###Plot of relative frequencies
You can use the function plot() to create a graphic with the relative frequencies of a series of rolling devices:

plot(roll100)

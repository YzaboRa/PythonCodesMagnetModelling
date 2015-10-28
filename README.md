# PythonCodesMagnetModelling

import csv
import math
import numpy
import array
import pylab

############################
#Load the matrix output by the radia code (2D)
############################

#>>> data = loadtxt("myfile.txt", delimiter=';')                   # use ';' as column separator instead of whitespace
#data=genfromtxt('data_test.txt')  #other possibility to import a matrix
data = numpy.loadtxt("??????.txt")                       # the array contains 3 columns of numbers?
x = data[:,0]                            # magnitude of the B-field 
z = data[:,1]                           #assosiated radius from the center of the magnet
Bmag = data[:,2]                           #assosiated angle

############################
#Correct for the actual position of the NV-center
############################

#The radia code assumes that the NV-center is at a distace (x,z) from the center of the magnet
#Need to measure the magnetic field at a certain (x0,z0) position, and compare it to the one predicted by the radia code
#Use the measurement value to correct the model

# Bmeasured1: measured strenght of the B-field
# x1: x-position (radial displacement) of the NV-center for Bmeasured1
# z1: z-position of the NV-center for Bmeasured1
 Bmeasured1
 x1
 z1
#**********************What about the angle?************************************

for i in xrange (0,(len(Bmag)-1)):
    if Bmag[i] == Bmeasured1:
        if Bmag.count(Bmeasured) == 1:
            deltax = x1 - x[i]
            break
        else:
            deltax.append(x1 - x[i])
minimum = deltax[1]
for j in xrange(0,len(deltax)):
    


############################
#Create a 3D matrix to store all the x,y,z and Bmagnitute parameters
############################

#store the size of the data array in the parameters a and b
(a,b)=data.shape
#initialize an empty 3D array, with dimensions  
numpy.zeros((a,b,a))


   

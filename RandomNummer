!/usr/bin/python3
# title             :Randomnummer.py
# description       :Linear Congruential Generator vergelijken met numphy
# ======================================================================================================================

# Importing libraries ==================================================================================================

import numpy
import time

# The actual script ====================================================================================================

# Parameters
hoeveelheid = 1000000
startgetal = 1
lijstMetGetallen = []

# LCG functie
def randomnummer(m=hoeveelheid, a=21, c=31, startgetal=startgetal):
    if len(lijstMetGetallen) == 0:
        lijstMetGetallen.append(startgetal) #Voor het vergelijken van de verschillende functies kunnen we geen variabele zoals de tijd tot input van de gebruiker toestaan
    else:
        lijstMetGetallen.append((a * lijstMetGetallen[-1] +c) % m)
    #print("lijst ", lijstMetGetallen)
    return lijstMetGetallen[-1]

# Code die genoeg getallen geneert voor LCG te kunnen timen
def runnerLCG():
    #print('LCG')
    for x in range(hoeveelheid):
        randomnummer()

# Code die genoeg getallen geneert voor NP te kunnen timen
def runnerNP():
    #print('Numpy')
    for x in range(hoeveelheid):
        numpy.random.randint(0, hoeveelheid)

start_time_LCG = time.time()
runnerLCG()
elapsed_time_LCG = time.time() - start_time_LCG

start_time_NP = time.time()
runnerNumpy()
elapsed_time_NP = time.time() - start_time_NP

print("Tijd voor LCG:", elapsed_time_LCG, "VS tijd voor Numpy:", elapsed_time_NP, "bij een run van", hoeveelheid)


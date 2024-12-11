# READ ME
https://github.com/windy-schmieder/CEE-4200-Final-Project.git \
Tomás Schmieder (tas274@cornell.edu) & Maoz Bizan (mb2389@cornell.edu)



Welcome to our final project for CEE 4200 Water Resources Management taught by Stefano Galelli at Cornell University!

This project consists of looking at the 2014-2016 drought in Brazil and adjusting the outflows of the reservoirs into the São Paulo Metropolitan Region (SPMR) to adapt the system better when there is a drought. This was done using a genetic algorithm made in Python using DEAP and several other modules. You can find these files in the repository. Within this readme file, we will go over what each of the files is and how to use them!

## Before we start

The files that we use are in the form of .ipynb, and can be run as Jupyter Notebooks or using an IDE. If there are packages that you do not have, here are the commands that are needed run the files. You can put them in your terminal:

  pip install deap \
  pip install pandas\
  pip install matplotlib\
  pip install numpy\
  pip install plotly\
  pip install random
  

## FILE #1: "data.csv"

This file is a csv that contains the data that we found through online databases and generated using InfeRes, and then used in our calculations and graphing. The columns are as follows:

  the date when the data was recorded \
  the change in time between dates \
  blank column \
  percent storage full \
  combined storage of the two reservoirs we used in mcm \
  combined precipitation of the two reservoirs we used in mcm \
  the inverted inflow in mcm (we calculated the inflow by inverting our mass balance equation as we had values for everything except inflows) \
  outflow in mcm based on the change in time between data points \
  blank column \
  blank column \
  outflow in mcm/day \
  outflow in m^3/s

The data consists of points from 1/1/10 - 11/12/19. The time step between each of the data points differs between each point, which is why the change in time column is present and is used in the calculations.

For the following files, **make sure that you replace the file_path at the beginning of the document with the file path of the data.csv file that you have downloaded.**
## FILE #2: "Resilience & Reliability Checker.ipynb"

This file allows you to calculate the average resilience and reliability of a specific contingency plan you input in the function of revised_outflow_policy. Currently, the values in this file represent that of the optimal contingency plan.

## File #3: "Genetic Algorithm.ipynb"

This file has two blocks in it. The first is the actual genetic algorithm that looks at an initial population of 1000 and goes through 250 generations, to then graph all of the individuals and create a pareto front showing the trade-off between resilience and reliability. \
The second block normalizes all of the individuals to be on a scale of (0,1). Normalizing the data so that it scales correctly enables our utopia point to be set to the maximum of (1,1). The code then calculates the distances between the individuals and the utopia point to find the one with the shortest distance, and that becomes our best individual. A graph representing the normalized data is produced, showing this point.

## File #4: "Graphing.ipynb

This file has three blocks in it. The first is code that creates a graph to compare the updated storage level and historical storage levels over time. This code also prints out all of its calculations for each iteration: this was used to debug the code and ensure that the correct number of iterations were used. We kept it in because it is helpful and shows how all the values change at each specific date. \
The second block is code that produces three graphs, the first being the historical storage level, the second being outflow over time, and the third being the drinking water deficit over time, the third block builds on this code using the new contingency plan. \
The third block is code that produes two graphs that compare the outflow and deficits over time for both the historical and new contingency plan. 

#### THANK YOU FOR A GREAT SEMESTER, PROFESSOR STEFANO!


# CPP-Projects: Cleaning Robot Simulation
This repository contains a series of exercises focused on developing and refining a cleaning robot simulation. The robot navigates and cleans a house represented as a text file. Each exercise builds upon the previous one, progressively enhancing the robot's intelligence and efficiency.

## Repository Structure
ex1/: Contains the code for the first exercise.
ex2/: Contains the code for the second exercise.
ex3/: Reserved for the third exercise (not yet uploaded).

## House Representation
The house is represented as a text file with the following characters:
'W': Walls that the robot cannot pass through.
Characters '0' to '9': Represent the level of dirt, with '0' being clean and '9' being very dirty.
'D': The docking station where the robot begins and ends its cleaning.
Exercise Details

## Exercise 1 (ex1/)
Objective: Implement a basic cleaning robot that navigates randomly.
Functionality: The robot moves randomly within the house, cleaning dirt as it encounters it. It has no strategy beyond random movement.

## Exercise 2 (ex2/)
Objective: Improve the robot's cleaning strategy using a grid-based approach.
Functionality: The robot moves in a more systematic manner, using grid-based logic to cover the house more efficiently compared to random movement.

## Exercise 3 (ex3/)
Objective: Implement two advanced algorithms to maximize cleaning efficiency.
Functionality: The robot uses two distinct algorithms to clean the house with the fewest steps possible, aiming to be as efficient as possible. The goal is to optimize the cleaning process and minimize energy consumption, increasing the chances of winning an efficiency competition.

## Constraints
Max Steps: The robot is limited by a maximum number of steps, which is defined in the input file.
Battery Life: The robot's battery life is also limited, necessitating careful management of its energy during cleaning.

## Input File Format
The input file should contain the following information:
1. MaxSteps - The Maximum number of steps allowed.
2. MaxBattery - The battery capacity. 
3. Rows - The number of rows in the home representation.
4. Cols - The number of columns in the home representation.
5. House layout:
   each char represents a dirt level (`0-9`), a wall (`W`), or the docking station (`D` - must have one).

## Output File Format
The program generates an output file which has the following data:
1. NumSteps - The number of steps taken.
2. DirtLeft - Remaining Dirt.
3. Status - FINISHED, WORKING or DEAD.
4. All steps performed:
- 'S' for South
- 'N' for north
- 'E' to the east
- 'W' for West
- 's' to stay
- 'F' to finish

### Input File - example (`inputfile.txt`)
```
1-Small house
MaxSteps=2210
MaxBattery = 60
Rows= 9
Cols=19
WWWWWWWW11119999999
W222WWW22222999D999
W33333333333WW999WW
444444444444499999W
WWW88855555WWWW999W
W6666W666666999W99W
W7777777777799WW99W
W4567WW2888899W999W
99999999999999WWWWW
```
### Output File - example (`output_inputfile.txt`)
```
NumSteps = 2163
DirtLeft = 0
Status = FINISHED
Steps:
NsssssssssEsssssssssEsssssssssEsssssssssSsssssssssWsssNWWSssssssssssssssssssssEsssssssssEssssssWSsssssssssSsssssssssEsssssssssSssssNWNNWssssssssssssssssssssSsssssssssSsssssssssSsssssssssEsssssssssEsssssSsssssNNWNNWssssssssssssssssssssWsssssssssNsssssssssWsssssssssSsssssssssWsssssssssNsssSEEEssssssssssssssssssssSWsssssssssSsssssssssWsssssssssWssssWssssNsssNssNsEsssSEEEssssssssssssssssssssNWWWsssWWsSssSsssSssssSsssssSssssssEssssssEssssWWNNNNEEEEEssssssssssssssssssssESSSSsssssssssEssssSsssssssssSsssssssssWsssssssssENNNNWNNWssssssssssssssssssssESSSSSsssssssssSWsssssssssENNNNWWWWWWWssssNsssNssNsSEEEEEEssssssssssssssssssssWWWWWWWssNsSSsssSssssSsssssEsssssSssssssSssssssNNNNNEEEEEEssssssssssssssssssssWWWWWWWWssSsssSssssSsssssSssssssEssssssSssssssNNNNNEEEEEEEssssssssssssssssssssSSWWWWWSSSsssssssEsssssssEsssssssssNsssssEssssWWWNNNNEEEEEssssssssssssssssssssWWWWSWWWWWsssSssssSsssssSssssssSsssssssEsssssNNNNNEEEEEEEEssssssssssssssssssssSSWWWWWSSSSssssssssEssssssssEsssssssssEsssssWNNWWNNNNEEEEEssssssssssssssssssssSSWWWWWSSSWsSssssssssSsssssssssEsssssssssEsssNNNWNNNNEEEEEssssssssssssssssssssWWWWSWWWWWWsssSssssSssssssssWssssssssNssssNsssEEENEEEEEEEEssssssssssssssssssssSSWWWWWSSEEEsssssEsssssssssWSsssssssssSssssSNNNWWWNNNNEEEEEssssssssssssssssssssSSWWWWWSSSWWsSssssssssSsssssssssWsssssssssNsNNNNNNEEEEEEEEssssssssssssssssssssSSWWWWWSSESSSssssssEsssssssssEsssssssssNWWWWWNNNNNNEEEEEEEssssssssssssssssssssSSWWWWWSSSWWWssSsSWsssssssssWsssssssssWsEEENNNNNNNEEEEEEEEssssssssssssssssssssWWWWSWWWWWWWWsssNssWssSsssSssssEssssSssssssNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSSSWWWWWsssssssWsssssssNssssssWssssNNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSWWWWWWWssSssSsssssssSssssssEsssssNNNNNEEENEEEEEEEEssssssssssssssssssssWWWWSWWWWWWWWWWsssNssSSssssWssssEEESSWsssENNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSSSWWWWWWSssSssssssssWsssssssssWENNNNNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSWWWWWWSWWsssSsssssssSsssssSsssNNNENNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSWWWWWWSWWWssssssSsssssssSssssSNNNEENNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSSSSSWWWWWWWWssssssWsssssssssWENNNEENNNEEEENEEEEEEEEssssssssssssssssssssSSWWWWWSSSSSWWWWWWWWWWsssssssssENNNEENNNEEEENEEEEEEEEF

```

## A representation of the house as the algorithm should refer to it during the run (from ex2)
```
currentLocation: layout[16][2] = D
number of steps so far = 0        
remainedSteps = 2210
totalDirt = 815
battery = 60
W W W W W W W W W W W W W W W W W W W W W 
W W W W W W W W W 1 1 1 1 9 9 9 9 9 9 9 W 
W W 2 2 2 W W W 2 2 2 2 2 9 9 9 D 9 9 9 W 
W W 3 3 3 3 3 3 3 3 3 3 3 W W 9 9 9 W W W 
W 4 4 4 4 4 4 4 4 4 4 4 4 4 9 9 9 9 9 W W 
W W W W 8 8 8 5 5 5 5 5 W W W W 9 9 9 W W 
W W 6 6 6 6 W 6 6 6 6 6 6 9 9 9 W 9 9 W W 
W W 7 7 7 7 7 7 7 7 7 7 7 9 9 W W 9 9 W W 
W W 4 5 6 7 W W 2 8 8 8 8 9 9 W 9 9 9 W W 
W 9 9 9 9 9 9 9 9 9 9 9 9 9 9 W W W W W W 
W W W W W W W W W W W W W W W W W W W W W
```


## Displaying the house after the algorithm has finished running (from ex2)
```
currentLocation: layout[16][2] = D
number of steps so far = 2163     
remainedSteps = 47
totalDirt = 0
battery = 7
W W W W W W W W W W W W W W W W W W W W W 
W W W W W W W W W                       W
W W       W W W                 D       W
W W                       W W       W W W 
W                                     W W
W W W W                 W W W W       W W
W W         W                   W     W W 
W W                           W W     W W
W W         W W               W       W W 
W                             W W W W W W
W W W W W W W W W W W W W W W W W W W W W
```

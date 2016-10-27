|--------------------------------------------------|
|Jimmy Huang	                    			   |
|CSE321 PROJECT 1				                   |
|DCAS						                       |
|--------------------------------------------------|

Description:

In designing the DCAS program, I decided to create a grid and each grid location will be a struct that holds information about each box. In doing so i can keep track where eveything on the grid is. Each drone holds its own information, where it knows its locations and all. When tracking avoidance it will check if a box on the grid is locked and if it is it will check around it for a free move. Then it returns in the same manner after delivering the package.


Files:

struct.h	//Struct for DCAS
drone.h/.c	//Drone movements
map.h/.c	//Map creation and DCAS controls
dcas.c		//main program to run DCAS


DCAS tower is located at grid point (0,0) marked by lowercase 'x' along with its four runways.

Grid by default is 51x51.


To run the program you may simply execute the file jimmyhua_proj1 with no arguments, it will default to level 2 but with 100 buildings. You can edit the speed the program runs by changing the sleep timing in map.c and dcas.c

					Arguments are accepted as following:

"jimmyhua_proj1 [1] [2] [3]"

Arguments after each argument is optional but if you use say [3] you must also pass in [1] and [2] where if you only want [1], then [2] and [3] are optional.

[1] = input for level you would like to test where level 0 = 0, level 1a = 1, level 1b = 2, and level 2 = 3.

[2] = input for amount of drones with 250 being the max.

[3] = input for amount of buildings with 250 being the max.


Note: At times the destination may conflict with buildings where it is completely blocked in or out by buildings. this is not very likly to happen but may and i havn't found a way to detect such a case yet.
You may restart the program for another set of random buildings.

Note 2: If there is a lag, and 1 drone is used as input, the map may not print.

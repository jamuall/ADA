
For mark 2:

Create a player and a Casino task.

A Casino takes random (float) time to open, after that prints “Casino: opened” and it checks for a player to enter. It can terminate (select with terminate) if nobody comes, it checks infinitely many times, if somebody came. If a player comes prints “Casino: a player got in” and prints “Casino: finished” when finished.

A player takes also random (float) time to arrive, it prints "player: arrived", then calls the Casino to play, tries to enter immediately (call with select of immediate meeting type), he tries 3 max times. If successful, he writes "player: got in" and finishes, and it does not try again. If not successful, tries max 3 times, if after 3 trials did not go in, prints “player: failed to enter”.

The main program prints "Game started".

Possible printings:

Game started

player: arrived

player: try again

player: try again

player: try again

player: failed to enter

player: finished

Casino: opened

OR

Game started

Casino: opened

player: arrived

Casino: a player got in

Casino: finished

player: got in

player: finished

 

For mark 3. (it is different from mark 2!!).

Convert the player task into a task type, with player name as a discriminant (the number of player transformed to String). Each player has a random Boolean to decide if he is going in or not (in both rounds) and tries to go in within 1 second (use the corresponding select).

If he goes in to Casino, he scores points (random value that he generates between 0 and 1000). He writes "player_name, he got points: " and the points value, and then he goes home.

If he couldn't go in, he tries once again after 1 second.

If never got in, he writes "player_name did not play" and goes home.

Create an array of 10 players in main, each created at 0.5 second intervals (the array index is the name of the player),

The Casino will allow a player to get in within 1 second, for up to 5 players, and will keep open for 15 seconds from the start (use Clock) after which closes. Print all activities, with the name of the players too.

A possible printing:

Game started

 1 player: arrived

Casino: opened

 2 player: arrived

Casino: a player got in

 1 player: got in score: 596

 1 player: finished

 3 player: arrived

Casino: a player got in

 3 player: got in score: 970

 3 player: finished

 4 player: arrived

Casino: a player got in

 4 player: got in score: 423

 4 player: finished

 5 player: arrived

 2 player: failed to enter

 2 player: finished

 6 player: arrived

 7 player: arrived

 8 player: arrived

Casino: a player got in

 8 player: got in score: 727

 8 player: finished

 9 player: arrived

 5 player: failed to enter

 5 player: finished

 10 player: arrived

Casino: a player got in

Casino: finished

 10 player: got in score: 679

 10 player: finished

 6 player: failed to enter

 6 player: finished

 7 player: failed to enter

 7 player: finished

 9 player: failed to enter

 9 player: finished

 

For mark 4:

Convert the Casino task into a task type, create an array of 3 Casinos pointer. Increase the number of players from 10 to 20, and each player should pick a random Casino (if he tries second time, he goes to the same casino). The main should create first the 3 casinos (no delay between) and then the 20 players.

A possible printing:

Game started

Casino: opened

Casino: opened

Casino: opened

 2 player: arrived

Casino: a player got in

 2 player: got in casino: 1 score: 305

 2 player: finished

 1 player: arrived

 3 player: arrived

 4 player: arrived

Casino: a player got in

 3 player: got in casino: 1 score: 577

 3 player: finished

 1 player: failed to enter

 1 player: finished

 5 player: arrived

Casino: a player got in

 5 player: got in casino: 1 score: 49

 5 player: finished

 6 player: arrived

 7 player: arrived

Casino: a player got in

 7 player: got in casino: 3 score: 896

 7 player: finished

 4 player: failed to enter

 4 player: finished

 8 player: arrived

Casino: a player got in

 8 player: got in casino: 1 score: 707

 8 player: finished

 9 player: arrived

 6 player: failed to enter

 6 player: finished

 10 player: arrived

 11 player: arrived

Casino: a player got in

 11 player: got in casino: 3 score: 248

 11 player: finished

 12 player: arrived

Casino: a player got in

 12 player: got in casino: 2 score: 185

 12 player: finished

Casino: a player got in

Casino: finished

 10 player: got in casino: 1 score: 144

 10 player: finished

 13 player: arrived

Casino: a player got in

 13 player: got in casino: 2 score: 105

 13 player: finished

 9 player: failed to enter

 9 player: finished

 14 player: arrived

 15 player: arrived

 16 player: arrived

Casino: a player got in

 14 player: got in casino: 2 score: 979

 14 player: finished

 17 player: arrived

Casino: a player got in

 17 player: got in casino: 2 score: 798

 17 player: finished

 19 player: arrived

 18 player: arrived

 20 player: arrived

Casino: a player got in

 20 player: got in casino: 3 score: 296

 20 player: finished

Casino: finished

Casino: finished

 

For mark 5.

A manager should keep monitoring the statistics for the gaming process. Create a protected manager that calculates the total number of players who got into any of the 3 casinos, and their all over total scored points. The main program after starting casinos and players, it delays 20s, and then prints the statistics (total players and total scores).

A possible printing:

Game started

 1 player: arrived

Casino: opened

Casino: opened

Casino: a player got in

 1 player: got in casino: 2 score: 957

 1 player: finished

Casino: opened

 3 player: arrived

Casino: a player got in

 3 player: got in casino: 2 score: 867

 3 player: finished

 2 player: arrived

Casino: a player got in

 2 player: got in casino: 1 score: 101

 2 player: finished

 4 player: arrived

 5 player: arrived

 6 player: arrived

Casino: a player got in

 4 player: got in casino: 2 score: 64

 4 player: finished

Casino: a player got in

 5 player: got in casino: 2 score: 760

 5 player: finished

 7 player: arrived

Casino: a player got in

 7 player: got in casino: 3 score: 450

 7 player: finished

Casino: a player got in

 6 player: got in casino: 3 score: 673

 6 player: finished

 8 player: arrived

 9 player: arrived

Casino: a player got in

Casino: finished

 9 player: got in casino: 2 score: 714

 9 player: finished

 10 player: arrived

Casino: a player got in

 10 player: got in casino: 3 score: 747

 10 player: finished

 11 player: arrived

Casino: a player got in

 11 player: got in casino: 3 score: 85

 11 player: finished

 12 player: arrived

Casino: a player got in

Casino: finished

 12 player: got in casino: 3 score: 252

 12 player: finished

 13 player: arrived

 14 player: arrived

 15 player: arrived

 17 player: arrived

 16 player: arrived

 18 player: arrived

 19 player: arrived

Casino: a player got in

 19 player: got in casino: 1 score: 133

 19 player: finished

Casino: a player got in

 18 player: got in casino: 1 score: 583

 18 player: finished

 17 player: failed to enter

 17 player: finished

 20 player: arrived

 16 player: failed to enter

 16 player: finished

Casino: finished

Manager:  13 players got in

Manager: total score 6386

Game over

<!--
Creator: <Name>
Location: SF
-->

![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

#Michael Rogachevsky: Racing Game

Reflection: This outline was difficult in some respects as the actual funtionality of the game is very simple. The most complex element is the randomization of key bindings to the board. 


### User Stories & Game Mechanics
1. The game would require **two players**, starting on opposite corners of a 12x12 square grid.
2. The objective is to race through the maze to get into the **finish zone** a 2x2 square in the center of the board.
3. There are no dedicated controls for either player, they only have to focus on the square N, E, S, W  relevent to their car.
4. To move from sqaure to sqaure the player will have to hit the corresponding key of the next adjacent square.
5. Cars would start out default imgs but additional imgs would be availble. For now, all the cars would function identically, but could be represented by any number of sprites.


### Data Structures 

* List the type of each property (number, boolean, `Card`, etc.).
* List the parameters that each method will take.
* Don't forget a constructor!

**Car**
 
`body` (Img link)

`moves` (function with callbacks)

- `checkMoves` (function)

- `moveCar` (function)

`whichPlayer` (obj)

**Player**

`controls` (obj)

**Maze**

`Square` (class)

 - `availMove` (arr)

`finishZone` (object)
 
 - `checkWinner` (function)

**Game**

`body selector` (function to select cars)

`display winner` (function)

`<btn>select car</btn>`

`<btn>start race</btn>` (function to unfreeze contols.)
### Development Stories

1. The game starts ready to play. Users find the board mapped and default color cars in their respective corners.
 * `<btn>start race</btn>` and `<btn>select car</btn>` are the only availble clickables.
 * Control keys are frozen. (.preventDefault()).  As the map is generated, each square is randomly assigned a keyboard key.

2. Once the start button is hit, 
 * a 3 second countdown timer starts.
 * After the 3 second countdown, the controls unlock and each player can start moving their car.

3. Each player races to get into the center.
	* As each car enters a new square, it will trigger the `checkMoves` fucntion on the car to look at each adjacent square to capture which button is mapped to which sqaure. 
	* Once a player hits a legal move key, the car will move to the indicated square.  

4. Success!
 * The finish zone will check for a winner on a keystroke that corresponds to a finish zone square. 
 * Once a winner is declared, a pop-up window will appear announcing who won with a Name label and a blown up image of the winning car.
  



###Potential Challenges / Development Questions

1. How to randomize the key assignments?


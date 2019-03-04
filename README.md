# DOWNFALL

### Purpose

* This is a [Tetris](https://tetris.wiki/) clone written for the javascript BBC micro model B emulator, [jsbeeb](https://bbc.godbolt.org/).

* It was written as an entry for the [2019 BASIC 10 liner contest](http://gkanold.wixsite.com/homeputerium/kopie-von-basic-10liners-2019) in category EXTREME-256. The rules state that none of the lines of code should exceed 256 characters: BBC BASIC limits lines to 239 characters.

### Theme

Confidence is plummeting as the British economy crashes to the ground. The situation demands grit and resolve: the national currency is falling through the floor, and although you hate the idea of it, you must exchange all of your money before it loses its value altogether. Successful play is rewarded with a patriotic anthem.

### Tips

`DOWNFALL` has no winners, only survivors. The best strategy is not to play. ;)

Gambling with the future of the country something that you *May* regret.

### Keys

*X* rotate anticlockwise  
*C* rotate clockwise  
*<* move left  
*>* move right  
*Space* drop piece

### Mechanics

The game has a simple scoring method rewarding multiple line clearances, [similar to the original](https://tetris.wiki/Scoring) but without bonus points for using the hard drop. A rotation system is implemented in which the *O* piece (square) does not change, but every other tetromino has 4 different positions rotated around one of its component squares. Other features include single piece preview, wall kicks, and a fixed lock delay. Every time 10 lines are cleared, the speed increases by 25%.

### Code summary

#### Line 0:  
* Initialize variables and store data.  
* `*TV 253` shifts the screen down 3 lines to hide on-screen memory glitches in the emulator.  

#### Line 1:  
* Initialize the screen.  
* Create array of pieces `t$(T%,Z%)` where `T%` is the tile shape and `Z%` is its orientation.  
* Store the piece data in locations following address `p=&A00`.

#### Line 2:  
* Set up the game screen and print a welcome message.  

#### Line 3:  
* Emit a hideously mangled snippet of the British national anthem.  
* Begin the game loop.  

#### Line 4:  
* Clear the game data.  
* Refresh the game screen.  
* Create the next tile and print it at the top of the screen.  

#### Line 5:  
* Find out if the newly-dropped tile is on top of existing tiles, and set `R%` accordingly.  
* Obtain user input.  

#### Line 6:  
* Check whether any move is possible, and go to line 9 if so.  
* Kick wall if necessary.  

#### Line 7:  
* Return to user input unless `F%` is set, indicating that the piece has stopped falling.  
* Count the number of completed lines and store in `F%`.  

#### Line 8:  
* Update the total number of lines cleared `D%`, the score `S%`, and round delay `W%`.  
* Print the score, highlight lines about to be cleared, then update the game data and screen.  

#### Line 9:  
* Move the piece.  
* Return to user input unless `R%` is set, indicating loss of life.  
* Update number of lives and restart game unless no lives left.  
* Update high score, print end message, and start a new game.  

### Variables

The built-in integer variables `A%`-`Z%` are heavily used to optimimze performance.

`A%,B%,C%` lines 4,5 user input 
`D%*` lines 2,6 = total number of lines cleared  
`E%` flag variable   
`F%` flag lines 5,6 = time for tetromino to move down; lines 7,8 = number of lines cleared in current round  
`G%` cached pointer to tetromino data  
`H%` high score    
`I%,J%` temporary index variables  
`K%` temporary variable  
`L%` number of lives remaining  
`M%` mask for identifying complete lines  
`N%` shape of next tetronimo  
`P%,Q%` temporary pointer variables  
`R%` flag: end of life
`S%` game score  
`T%` tetromino shape  
`U%` time at last round  
`W%` length of round in units of 0.01s governing game speed  
`X%,x%` x location of tetromino (origin = left)  
`Y%,y%` y location of tetromino (origin = top)  
`Z%,z%` orientation of tetromino (start = 0)  

### Cheats

Here are couple of cheats, for those who like to tinker with the code:

* *Halve speed increases:* Change `W%=z*.75^(D%DIVe)` to `W%=z*.87^(D%DIVe)` in line 8.  
* *Infinite lives:* Remove `L%=L%-1` in line 9.  


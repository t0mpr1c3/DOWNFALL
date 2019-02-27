# DOWNFALL

### Theme

Confidence is plummeting as the British economy crashes to the ground. Exchange the falling currency before it loses all its value!

### Tips

DOWNFALL has no winners. But if you achieve the high score, you will learn the message of DOWNFALL.

### Keys

*A* rotate anticlockwise  
*B* rotate clockwise  
*<* move left  
*>* move right  
*Return* soft drop

### Mechanics

The game has a simple scoring method rewarding multiple line clearances, similar to the [original](https://tetris.wiki/Scoring) but without the bonus points for hard drop. A rotation system is implemented in which the *O* piece (square) does not change, but every other tetromino has 4 different positions rotated around one of its component squares. Other features include single piece preview, wall kicks, and a fixed lock delay.

### Variables

*A%,B%,C%* user input  
*D%* total number of lines cleared
*E%* flag: tetromino has stopped moving in y direction  
*F%* flag, number of lines cleared  
*G%* points scored for 1,2,3,4 lines  
*H%* flag: end of life  
*I%,J%* temporary index variables  
*K%* temporary variable  
*L%* lives  
*M%* mask for identifying tiles  
*N%* index of next tetronimo  
*P%,Q%* temporary pointer variables  
*R%* high score  
*S%* game score  
*T%* tetromino index  
*U%* time at last round  
*W%* length of round in units of 0.01s governing game speed  
*X%,x%* x location of tetromino (origin = left)  
*Y%,y%* y location of tetromino (origin = top)  
*Z%,z%* orientation of tetromino (start = 1)  

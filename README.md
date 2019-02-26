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
*Shift* soft drop

### Mechanics

Simple scoring as per the [original BPS](https://tetris.wiki/Scoring), except there are no bonus points for hard drop, as only soft drop is implemented. The rotation system also is similar to the original, with the exception that the I tetromino has 4 positions rather than 2. Single preview. Wall kicks, no floor kicks, fixed lock delay.

### Variables

*A%,B%,C%* user input  
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
*X%* x location of tetromino (origin = left)  
*Y%* y location of tetromino (origin = top)  
*Z%* orientation of tetromino (start = 1)  

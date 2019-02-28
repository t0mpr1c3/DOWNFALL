# DOWNFALL

### Theme

Confidence is plummeting as the British economy crashes to the ground. The situation demands grit and resolve: the national currency is falling through the floor, and although you hate the idea of it, you must exchange all of your money before it loses its value altogether. Successful play is rewarded with a patriotic anthem.

### Tips

DOWNFALL has no winners, only survivors. The best strategy is not to play.

Gambling with the future of the country something that you *May* regret.

### Keys

*X* rotate anticlockwise  
*C* rotate clockwise  
*<* move left  
*>* move right  
*Return* soft drop

### Mechanics

The game has a simple scoring method rewarding multiple line clearances, similar to the [original](https://tetris.wiki/Scoring) but without the bonus points for hard drop. A rotation system is implemented in which the *O* piece (square) does not change, but every other tetromino has 4 different positions rotated around one of its component squares. Other features include single piece preview, wall kicks, and a fixed lock delay.

### Variables

*A%,B%,C%* lines 4,5 user input; lines 0,1 = temporary data store  
*D%* lines 2,6 = total number of lines cleared; lines 0,1 = temporary data store  
*E%* flag: line 6 = tetromino has stopped moving in y direction   
*F%* flag: line 5 = time for tetromino to move down; lines 6,8,9 = number of lines cleared in current round  
*G%* data: points scored for 1,2,3,4 lines  
*H%* flag: end of life  
*I%,J%* temporary index variables  
*K%* temporary variable  
*L%* number of lives remaining  
*M%* mask for identifying complete lines  
*N%* shape of next tetronimo  
*O%* cached pointer to tetromino data  
*P%,Q%* temporary pointer variables  
*R%* high score  
*S%* game score  
*T%* tetromino shape  
*U%* time at last round  
*W%* length of round in units of 0.01s governing game speed  
*V%* length of delay before restarting game  
*X%,x%* x location of tetromino (origin = left)  
*Y%,y%* y location of tetromino (origin = top)  
*Z%,z%* orientation of tetromino (start = 0)  

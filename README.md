# Knight-tour-problem
** Please contact on following link if you want help on following knight tour problem **

** I will also help with C++ code **

Link to help: https://www.fiverr.com/s/x4N6e4

Introduction
The Knight's Tour Problem is a classic computer science problem that asks for a sequence of moves of a knight on a chessboard such that the knight visits every square only once. This assignment asks you to write a program that, given the board size, and a starting square and ending square, finds a knight's tour from the start to the end. Each square on the board must be used at most once. The knight's tour does not have to be the shortest possible. Any tour without repeating squares will be fine.

Requirements
The program must read the problem description (board size, start square, end square) from the command line parameters.
The program must check the command line parameters for correctness before starting to compute. There must be exactly three command line parameters, the first one an integer between 1 and 26, and the other two valid names for squares (a1 to z26, taking into account the board size from the first parameter).
If a knight's tour could not be found, the program must print the error message could not find a knight's tour.
If a knight's tour is found, the program must print the tour as a sequence of square names.
Example runs
./knight 3 a1 c3
a1 c2 a3 b1 c3

./knight 2 a1 b2
could not find a knight's tour

./knight 8 d3 h8
d3 b2 a4 c5 a6 c7 a8 b6 d7 b8 c6 a5 c4 a3 c2 a1 b3 d4 b5 a7 c8 e7 d5 b4 a2 c3 b1 d2 f3 e1 g2 e3 d1 f2 e4 d6 b7 d8 f7 e5 g6 h8

./knight 14 k13 a1
k13 i12 g11 e10 c9 a8 c7 a6 c5 a4 c3 a2 c1 b3 a1


## Error handling

./knight
invalid parameter list
./knight 8
invalid parameter list
./knight 8 a1
invalid parameter list
./knight 8 a1 b1 c1
invalid parameter list
./knight a1 a1 b1
invalid parameter list
./knight 4 a1 a5
invalid parameter list
./knight 4 d4 e4
invalid parameter list

Hint
You can interpret the command line parameters by creating an istringstream for each of them and reading into char and int variables from those streams.

Algorithm
To find a knight's tour, implement a recursive function that implements backtracking. The function should take the following parameters:

board: A 2D vector representing the chessboard.
startSquare: The starting square for the knight's tour.
endSquare: The ending square for the knight's tour.
The function should return true if a knight's tour is found, and false otherwise.

The function should work as follows:

If the start square is the same as the end square, then the tour is complete and the function should return true.
Iterate over all possible knight's moves from the start square.
For each move, check if the destination square is valid (within the board boundaries and not yet visited). If it is, then mark the square as visited and call the recursive function again, passing in the destination square as the new start square.
If the recursive function call returns true, then the tour is complete and the function should return true.
Otherwise, remove the mark from the destination square and continue iterating over the possible moves.
If the function returns false, then no knight's tour could be found.

Topics to exercise
Recursive functions
Command line parameters (stringstreams)
Error handling (likely with exceptions)
To use and not to use
For comparison

Use: all you need for finding a knight's tour is (2D-) vectors. If you are already comfortable with classes, you may use them, too. But if you use classes, use them well!
Implementing a recursive function according to the above pseudo code is mandatory!
The following constructs must not be used: arrays (except:argv), structs, pointers

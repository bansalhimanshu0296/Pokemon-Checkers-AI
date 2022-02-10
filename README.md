# Pokemon-Checkers-AI #

This project was done as a part of CSCI-B-551 Elements of Artificial Intelligence Coursework under Prof. Dr. David Crandall.

## Command to run the program ##

python3 ./raichu.py [board_size] [piece color] [current board configuration] [time for finding step]

## Observation ##

It is a modified checkers game and therefore we are expected to use a minimax based algorithm.

## State space ## 
Boards that being traversed in the game.

## Initial state ## 
Board Configuration for which we want to find next move.'

## Goal state ##
The board with the best move which we can reach from the initial input board.

## Successor state ##
The very next set of boards that can be achieved from the initial input board.

## Utility/Evaluation function ## 
(Number of AI pieces - Number of opponent pieces) * 500 + Number of AI pieces * 50.

## Approach and design decisions ##

**Abstraction technique:** Alpha-beta pruning with definite depth (constrained alpha-beta pruning)

Initially we convert the board string into a two dimensional matrix. We find all the successor states and run alpha-beta pruning on each of the successor states to find the highest alpha value. We are setting max value as the alpha value when alpha value is greater than max value and we yield that board. We are implementing the alpha-beta pruning algorithm using depth equating to 4. We define a ‘get_move’ function in which we are finding all the moves, i.e., pichu, pikachu and raichu, for a given board.

## Challanges ##

The main challenge was to find the utility function and depth upto which we have to run alpha-beta pruning to get the results within 10 seconds. Another challenge was constructing the ‘get_move’ function for the board.



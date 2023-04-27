# AI Tic-Tac-Toe opponent player game (NxN size)

A NxN Tic Tac Toe opponent player game using minimax algorithm with alpha beta pruning heuristics and iterative deepening search. 
The user will be able to play the game with an AI search agent by choosing the cells to make a move on or able to simulate a game automatically as well. The Game board is nxn size instead of a traditional 3x3 size, and the size of the board can be changed manually. The user or the AI wins if there is a consecutive line or a diagonals with their character “X” or “O”. The game will be a draw if no consecutive line is filled by one of the player.

# **Solution Specification**

The game implementation uses **Minimax algorithm with alpha-beta pruning and iterative deepening search**. Each of the parts will be explained here:

## *Minimax algorithm*

How Minimax algorithm works is it tries to minimize the opponent’s utility while maximizing its own utility for the AI. By using the algorithm, we try to find out the best possible move to make based on each game state, which should be valid but also maximizing the utility. When we run the algorithm, we give a time limit for the AI (value for AItimer parameter in TicTacToe class) to make the best possible move within the time limit. One issue with only implementing a minimax algorithm is, as mentioned above, the number of game states we have to check increases exponentially. That is when we need Alpha-beta pruning.

## *Alpha Beta Pruning*

It is an optimization heuristics to make the Minimax algorithm more efficient. It does not check all the possible states, but instead it will prune the states that are already guaranteed to be a non-optimal state for the current player - max or min. It helps us to cut a lot of time that can be spent on checking a non-optimal path. The alpha-beta pruning is going to return the same value that the minimax algorithm returns, but it is going to help us cut nodes that are making the algorithm slower by pruning them.

## *Iterative Deepening Search*

The way this iterative deepening search is implemented is it is meant to find the shortest path within the give time frame to find the best possible moves for the AI player side. Since we have complication when we increase the board size, there is more depth to check down the tree. I have applied a time limit where they check for the best possible moves within the constraint.

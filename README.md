# AI-Based-Chess-Engine

User-friendly setup for game of chess using various existing data structures and algorithms.

## Data Structure Used:

2D Array: To make the game board and store the positions of the chess pieces.
Tuple: To keep track of player clicks to make valid moves
Tree: Chess programs consider chess moves as a game tree. They examine all moves, then all counter-moves to those moves, then all moves countering them, and so on, where each individual move by one player is called a "ply". This evaluation continues until a certain maximum search depth or the program determines that a final "leaf" position has been reached (e.g. checkmate).

## Algorithm Used:

NAÏVE ALGORITHM : Naïve Bayes classifiers are linear classifiers based on Bayes’ theorem. The model generated is probabilistic. It estimates conditional probability which is the probability that something will happen, given that something else has already occurred.
GREEDY ALGORITHM : A Greedy algorithm is an algorithmic paradigm that follows the problem solving heuristic of making the locally optimal choice at each stage with the hope of finding a global optimum
MIN-MAX ALGORITHM : Min-max is a kind of backtracking algorithm that is used in decision making and game theory to find the optimal move for a player, assuming that your opponent also plays optimally

## Tree generation:
The tree generator component of the chess AI generates the possible future board positions based on the possible moves that the pieces can make. At any given position, there are on average 20 possible moves that can be made in chess.

![image](https://user-images.githubusercontent.com/65500415/168745684-ceacdf9e-616a-44ec-8be4-373cc9b83ea5.png)


The above illustrates a chess tree. Possible moves are generated from the current position to create hypothetical future states.

## Minimax algorithm:
The minimax algorithm tries to find the optimal move from a tree of moves. Starting from the leaves of the tree which represent future states, you want to propogate back to the present root node by alternating between min() and max() (hence the name, minimax).

When it is your turn, you want to optimize for your outcome, therefore you want to calculate the max() position score.

When it is your opponents turn, he wants to minimize your outcome, therefore it calculates the min() position score.

![image](https://user-images.githubusercontent.com/65500415/168746911-50622f64-09fc-46ac-a02d-153d0e3674d4.png)

## Alpha-beta pruning:
Alpha-beta pruning is a process that can be used to greatly reduce the space of the tree search. It works by pruning the search tree as you generate it by ruling out paths that neither you nor your opponent will never take.

This is done by keeping track of two values called alpha and beta as you are searching through the tree.
Alpha is the maximum lower bound (the lowest score you are willing to accept)
Beta is the minimum upper bound (the highest score your opponent is willing to accept)

The guide below explains alphabeta pruning very well: http://web.cs.ucla.edu/~rosen/161/notes/alphabeta.html

## Special Moves:

CASTLING : It is a special rule that allows your king to move two spaces to its right or left, while the rook on that side moves to the opposite side of the king.
EN PASSANT : En passant is a capture by a pawn of a horizontally adjacent enemy pawn that has just advanced two squares in one move.
PAWN PROMOTION :Pawn Promotion is the replacement of a pawn with a new queen, rook, bishop, or knight of the same color . It occurs immediately when the pawn moves to its last rank .
![image](https://user-images.githubusercontent.com/65500415/168745535-6ca319c4-d277-4d8f-8431-d3c994c4eaf1.png)

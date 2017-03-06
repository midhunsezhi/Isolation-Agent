
# Game-playing Agent for Isolation

## Synopsis

This is an adversarial search agent to play the game "Isolation".

Isolation is a deterministic, two-player game of perfect information in which the players alternate turns moving a single piece from one cell to another on a board.  Whenever either player occupies a cell, that cell becomes blocked for the remainder of the game.  The first player with no remaining legal moves loses, and the opponent is declared the winner.

This project uses a version of Isolation where each agent is restricted to L-shaped movements (like a knight in chess) on a rectangular grid (like a chess or checkerboard).  The agents can move to any open cell on the board that is 2-rows and 1-column or 2-columns and 1-row away from their current position on the board. Movements are blocked at the edges of the board (the board does not wrap around), however, the player can "jump" blocked or occupied spaces (just like a knight in chess).

## Procedure used to develop the agent:

This agent uses iterative deepening to get the next move by searching the game tree to various depth levels and returns the best found move before the timer expires.

The game tree is searched using depth-limited Minimax Search, which is further improved with alpha-beta pruning.

I developed various heuristics and scored them against each other to effectively get the Utility value of a node at the end of the depth-limited search.
The basic idea behind each of these heuristics is to reward the player for his available moves and penalize based on his opponent moves.
 
10-04-2023
---
# Chapter 6 - Game Playing

## Games vs. search problems

"Unpredictable" opponent $\rightarrow$ solution is a strategy specifying a move for every possible opponent reply.

Time limits $\rightarrow$ unlikely to find goal, must approximate

## Types of games
/ | deterministic | change
--- | --- | ---
perfect information | chess, checkers, go, othello | backgammon, monopoly
imperfect information | battleships, blind tictactoe | bridge, poker, scrabble, nuclear war

## Minimax
Perfect play for deterministic, perfect-information games

Idea: choose move to position with highest *minimax value* = best achievable payoff against best play.
Minimize opponent utility, maximize own utility

### Properties
Complete?
- Yes, if tree is finite (chess has specific rules for this)

Optimal?
- Yes, against an optimal opponent

Time complexity?
- $O(b^m)$

Space complexity?
- $O(bm)$ (depth first exploration)
For chess, b ~ 35, m ~ 100 for "reasonable" games

### $\alpha - \beta$ pruning
Pruning does not affect final result

Good move ordering improves effectiveness of pruning

With "perfect ordering," time complexity = $O(b^{\frac{m}{2}}) \rightarrow$ doubles solvable depth

Does not make every problem solvable in "reasonable" time, chess is still very hard with pruning

#### Resource limits
Standard approach:
Use Cutoff-Test instead of Terminal-Test, e.g. depth-limit (perhaps add *quiescence search*)

Use Eval instead of Utility, i.e., *evaluation function* that estimates desirability of position

#### Evaluation functions
For chess, typically linear weighted sum of features

Exact values don't matter. Behavior is preserved under any monotonic transformation of Eval

Only the order matters:
- payoff in deterministic games acts as an ordinary utility function

## Nondeterministic games in general
Chance introduced by dice, card-shuffling

Expectiminimax gives perfect play.
Just like Minimax, but we must also handle chance nodes

## Games of Imperfect Information
E.g. card games, where opponent's initial cards are unknown.

Typically we can calculate a probability for each possible deal.

Seems just like having one big dice roll at the beginning of the game.

Idea: compute the minimax value od each action in each deal, then choose the action with highest expected value over all deals.

Special case: if an action is optimal over all deals, it's optimal.
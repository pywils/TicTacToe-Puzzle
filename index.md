[#nba-tanking]
(#tictactoe-puzzle)

(#tictactoe-puzzle)
# TicTacToe Puzzle from FiveThirtyEight

## Question:
A local cafe has board games on a shelf, designed to keep kids (and some adults) entertained while they wait on their food. One of the games is a tic-tac-toe board, which comes with nine pieces that you and your opponent can place: five Xs and four Os.
When I took my two-year-old with me, he wasn’t particularly interested in the game itself, but rather in the placement of the pieces.
If he randomly places all nine pieces in the nine slots on the tic-tac-toe board (with one piece in each slot), what’s the probability that X wins? That is, what’s the probability that there will be at least one occurrence of three Xs in a row at the same time there are no occurrences of three Os in a row?

## Answer: 
Let’s take a look at how many winners there are for Xs, how many winners there are for Os, how many tie games there are, and how many times both Xs and Os win.

If we randomly assorted five Xs and four Os on a tic-tac-toe board, there would be 126 different possible outcomes.

|                        | Only Xs win   | Only Os win  |   Cats games  | Both Xs and Os win  |
| ---------------------- | ------------- | -------------| ------------- | ------------------- |
| Number of scenarios    |      62       |      12      |       16      |           36        |
| Probability of winning |      0.49     |      0.1     |       0.13    |           0.29      |

 

Now then, let’s visualize the different scenarios. First, let’s look at all the cases in which the “X” player wins and the “O” player does not.
```
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "X"  "0"  "0"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "X"  "0"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "X"  "0"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "X"  "0"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "0"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "X"  "0"  "0"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "X"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "X"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "X"  "0"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "X"  "0"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "X"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "0"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "X"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "X"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "0"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "X"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "X"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "X"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "0"  "X"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "0"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "X"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "X"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "X"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "0"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "X"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "0"  "X"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "0"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "X"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "X"  "0"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "X"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "0"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "0"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "X"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "0"  "X"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "X"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "X"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "0"  "X"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "X"  "0"  "0"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "X"  "0"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "X"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "X"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "X"  "0"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "X"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "0"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "X"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "0"  "X"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "X"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "0"  "X"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "X"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "X"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "0"  "0"  "X"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "0"  "0"  "X"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "0"  "X"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "0"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "0"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "0"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "X"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "X"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "0"  "X"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "0"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "0"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "0"  "0"  "X"
## [3,] "X"  "X"  "X"
```
Now let’s look at cases for which the “0s” win and the “Xs” do not.
```
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "0"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "0"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "0"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "0"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "0"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "0"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "0"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "0"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "0"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "0"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "0"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "0"  "X"
## [3,] "0"  "X"  "X"
```
Now let’s look at cases which are cats:
```
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "X"  "0"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "X"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "0"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "0"  "X"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "0"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "0"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "X"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "X"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "0"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "X"  "0"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "0"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "0"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "X"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "0"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "0"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "0"  "X"  "X"
## [3,] "X"  "0"  "X"
```
Now let’s look at outcomes in which both Xs and Os win:
```
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "X"  "0"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "0"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "X"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "X"  "0"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "X"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "X"  "X"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "X"  "X"  "0"
## [3,] "0"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "0"  "0"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "X"  "X"  "X"
## [3,] "0"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "0"
## [2,] "X"  "X"  "X"
## [3,] "X"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "0"  "X"
## [3,] "X"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "X"  "0"  "X"
## [3,] "0"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "X"  "X"
## [3,] "0"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "X"  "X"
## [3,] "0"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "X"  "X"  "X"
## [3,] "0"  "0"  "0"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "X"  "X"
## [3,] "0"  "X"  "0"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "0"
## [2,] "0"  "0"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "0"
## [2,] "X"  "X"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "0"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "0"  "0"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "0"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "X"  "X"
## [2,] "0"  "0"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "0"  "0"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "X"  "0"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "0"
## [2,] "X"  "0"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "0"
## [2,] "X"  "X"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "0"
## [2,] "X"  "0"  "X"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "0"
## [2,] "X"  "X"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "0"
## [2,] "0"  "X"  "X"
## [3,] "X"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "0"
## [2,] "0"  "X"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "X"  "0"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "X"  "0"  "X"
## [2,] "0"  "0"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "X"  "0"  "X"
## [3,] "X"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "X"  "X"
## [3,] "0"  "0"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "X"  "X"
## [2,] "0"  "0"  "X"
## [3,] "0"  "X"  "X"
##      [,1] [,2] [,3]
## [1,] "0"  "0"  "X"
## [2,] "0"  "X"  "X"
## [3,] "0"  "X"  "X"
```
Code as reference:
```
n = 9
possibleCombinations <- expand.grid(replicate(n, 0:1, simplify = FALSE))
sumPossibleCombinations <- apply(possibleCombinations, 1, sum)
possibleCombinationsSumFive <- rep(0, dim(possibleCombinations)[1])

# Only include possible combinations that have 5 Xs (represented by 1s) and 4 0s
for(i in 1:dim(possibleCombinations)[1]) {
if (sumPossibleCombinations[i] == 5) {possibleCombinationsSumFive[i] <- sumPossibleCombinations[i]}
else {possibleCombinationsSumFive[i] <- NA}
}

df <-cbind(possibleCombinations, possibleCombinationsSumFive)


#Removing the NAs
dfWithoutNAs <-df[complete.cases(df[ , 10]),]


#we'll create an object that will track who will win.
winner <- rep(0, dim(dfWithoutNAs)[1])
winner <- cbind(winner, winner)


#There are a number of different ways to win in tic-tac-toe
for (i in 1:dim(dfWithoutNAs)[1]) {
#winning the top 3
if(dfWithoutNAs[i, 1] == 1 & dfWithoutNAs[i, 2] == 1 & dfWithoutNAs[i, 3] == 1)
{winner[i] <- 1}
#winning the middle 3
if(dfWithoutNAs[i, 4] == 1 & dfWithoutNAs[i, 5] == 1 & dfWithoutNAs[i, 6] == 1)
{winner[i] <- 1}
#winning the bottom 3
if(dfWithoutNAs[i, 7] == 1 & dfWithoutNAs[i, 8] == 1 & dfWithoutNAs[i, 9] == 1)
{winner[i] <- 1}
#winning the top left to bottom right diagonals
if(dfWithoutNAs[i, 1] == 1 & dfWithoutNAs[i, 5] == 1 & dfWithoutNAs[i, 9] == 1)
{winner[i] <- 1}
#winning the top right to bottom left diagonals
if(dfWithoutNAs[i, 3] == 1 & dfWithoutNAs[i, 5] == 1 & dfWithoutNAs[i, 7] == 1)
{winner[i] <- 1}
#winning the left three
if(dfWithoutNAs[i, 1] == 1 & dfWithoutNAs[i, 4] == 1 & dfWithoutNAs[i, 7] == 1)
{winner[i] <- 1}
#winning the middle three
if(dfWithoutNAs[i, 2] == 1 & dfWithoutNAs[i, 5] == 1 & dfWithoutNAs[i, 8] == 1)
{winner[i] <- 1}
#winning the right three
if(dfWithoutNAs[i, 3] == 1 & dfWithoutNAs[i, 6] == 1 & dfWithoutNAs[i, 9] == 1)
{winner[i] <- 1}
}


#NOW FOR THE Os winning

for (i in 1:dim(dfWithoutNAs)[1]) {
#winning the top 3
if(dfWithoutNAs[i, 1] == 0 & dfWithoutNAs[i, 2] == 0 & dfWithoutNAs[i, 3] == 0)
{winner[i, 2] <- 1}
#winning the middle 3
if(dfWithoutNAs[i, 4] == 0 & dfWithoutNAs[i, 5] == 0 & dfWithoutNAs[i, 6] == 0)
{winner[i, 2] <- 1}
#winning the bottom 3
if(dfWithoutNAs[i, 7] == 0 & dfWithoutNAs[i, 8] == 0 & dfWithoutNAs[i, 9] == 0)
{winner[i, 2] <- 1}
#winning the top left to bottom right diagonals
if(dfWithoutNAs[i, 1] == 0 & dfWithoutNAs[i, 5] == 0 & dfWithoutNAs[i, 9] == 0)
{winner[i, 2] <- 1}
#winning the top right to bottom left diagonals
if(dfWithoutNAs[i, 3] == 0 & dfWithoutNAs[i, 5] == 0 & dfWithoutNAs[i, 7] == 0)
{winner[i, 2] <- 1}
#winning the left three
if(dfWithoutNAs[i, 1] == 0 & dfWithoutNAs[i, 4] == 0 & dfWithoutNAs[i, 7] == 0)
{winner[i, 2] <- 1}
#winning the middle three
if(dfWithoutNAs[i, 2] == 0 & dfWithoutNAs[i, 5] == 0 & dfWithoutNAs[i, 8] == 0)
{winner[i, 2] <- 1}
#winning the right three
if(dfWithoutNAs[i, 3] == 0 & dfWithoutNAs[i, 6] == 0 & dfWithoutNAs[i, 9] == 0)
{winner[i, 2] <- 1}
}

#create table

cats <- winner[, 2] == 0 & winner[, 1] == 0

bothWin <- (winner[,1]) == 1 & winner[, 2] == 1

xWin <- (winner[,1]) == 1 & winner[, 2] == 0
oWin <- (winner[,1]) == 0 & winner[, 2] == 1

numberOfWins <- c(sum(xWin), sum(oWin), sum(cats), sum(bothWin))

winProbability <- c(sum(xWin)/dim(winner)[1], sum(oWin)/dim(winner)[1], sum(cats)/dim(winner)[1], sum(bothWin)/dim(winner)[1])

table <- rbind(numberOfWins, round(winProbability, 2))
colnames(table) <- c("Xs win", "0s win", "Cats games", "Both Xs and 0s win")
rownames(table) <- c("number of scenarios", "Probability of Winning")

table

 

 

#output outcomes in which only Xs win

dfWithoutNAs <- dfWithoutNAs [,-10]

for(i in 1:dim(dfWithoutNAs[1])){
  dfWithoutNAs[i,] <- gsub(1, "X", dfWithoutNAs[i, ])
}


for(i in 1:dim(dfWithoutNAs)[1]) {
if (winner[i] == 1 & winner[i, 2] == 0) {print(matrix(dfWithoutNAs[i, ], ncol=3))}
}

 

#output outcomes in which only Os win

for(i in 1:dim(dfWithoutNAs)[1]) {
if (winner[i, 2] == 1 & winner[i] == 0) {print(matrix(dfWithoutNAs[i, ], ncol=3))}
}

 

#output outcomes in which no one wins

for(i in 1:dim(dfWithoutNAs)[1]) {
if (cats[i] == "TRUE") {print(matrix(dfWithoutNAs[i, ], ncol=3))}
}

#output outcomes in which both Xs and Os win

for(i in 1:dim(dfWithoutNAs)[1]) {
if (bothWin[i] == "TRUE") {print(matrix(dfWithoutNAs[i, ], ncol=3))}
}
```

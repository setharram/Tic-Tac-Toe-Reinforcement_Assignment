# Tic-Tac-Toe-Reinforcement_Assignment

One of the most popular and enduring games of all time is Tic-Tac-Toe. Because of its familiarity, this game is often used as a starting example to mathematically analyze a decision-making process. Its brevity makes it a perfect game to illustrate the rewards of thinking ahead and learning the consequence of each decision.

Above TicTacToe_Agent.ipynb is Numerical Tic-Tac-Toe game. Instead of X’s and O’s, the numbers 1 to 9 are used.
In the 3x3 grid, numbers 1 to 9 are filled, with one number in each cell. 
* The first player plays with the odd numbers, 
* the second player plays with the even numbers, i.e. player 1 can enter only an odd number in the cell while player 2 can enter an even number in one of the remaining cells. 
* Each number can be used exactly once in the entire grid. The player who puts down 15 points in a line - (column, row or a diagonal) wins the game.

Objective of this notebook:- 
* Build MDP for Numerical Tic-Tac-Toe game. you can find it in TicTacToe() class:
* Action space for each state. need to make sure The actions are not the same for each state
* def for Winning states: the sum of three numbers in a row, column or diagonal is 15.
* def the terminal states (win,tie,loss) / also is Agent won or Environment won or ended up in tie

Agent Reward structure is as below:
* +10 if the agent wins (makes 15 points first across column, row or diagonal)
* -10 if the environment wins
* 0 if the game ends in a draw (no one is able to make 15 and the board is filled up)
* -1 for each move agent takes

Step function which takes in an input of the agent’s action and state; and outputs the next state and reward. 

In this agent learns the game by Q-Learning method. 
below are the hyperparameters 
* epsilon (decay rate),
* learning-rate,
* discount factor.

I have randomly pick up the value, one can futher tune, and can find the which factor contribute more for new Q dictionary update and state/action reward accuracy. 

Valuation:- 
Graph to show Q-values convergence- check whether Q-values learnt by the agent have converged or not. Sample 4 state-action pairs and plot it with the number of episodes to understand the convergence.
this is make sure model is learning in positive direction. 

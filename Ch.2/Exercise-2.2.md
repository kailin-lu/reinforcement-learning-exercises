# Exercise 2.2 Bandit Example 

Consider a k-armed bandit problem with k = 4 actions, denoted 1, 2, 3, and 4. 

Consider applying to this problem a bandit algorithm using $\epsilon$-greedy action selection, sample-average action-value estimates, and initial estimates of Q1(a) = 0, for all a. 

Suppose the initial sequence of actions and rewards is 

A1 = 1, R1 = −1, 
A2 = 2, R2 = 1, 
A3 = 2, R3 = −2,
A4 = 2, R4 = 2, 
A5 = 3, R5 = 0. 

On some of these time steps the $\epsilon$ case may have occurred, causing an action to be selected at random. 
On which time steps did this definitely occur? 

On which time steps could this possibly have occurred?

*Answer:* 

Make a table of estimated values at each time step. 

| t   | a1  | a2  |a3  | a4  |
|---  |---  |---  |--- |---  |
| 1   | -1  |  0  | 0  |  0  |
| 2   | -1  |  1  | 0  |  0  |
| 3   | -1  |-.5  | 0  |  0  |
| 4   | -1  | .3  | 0  |  0  |
| 5   | -1  | .3  | 0  |  0  |


The $\epsilon$ case definitely occurred at t=5 because a3 was chosen even though a2 had the highest sample average.  

It might have occurred at t=1, 2, 3, 4 even though the algorithm chose the highest value action, we do not know if this was due to random chance or not. 


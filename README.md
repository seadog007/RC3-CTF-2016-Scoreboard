# RC3-CTF-2016-Scoreboard

## Basic Concept
Basically, the score is under the structure of a user
So when I migrate a person who already solved the problem in the team to another team
Then the score will be double for questions.

## PoC
Create `Account A`, `Account B`.  
`A`: Create `Team α`.  
`B`: Create `Team β`.  
`A`, `B` solved a question which is 100 points.  
`B` remove himself from the `β`, which also delete the team.  
`B` join the `α`.
Now, Team `α` has two people who already solved the question, so the team got 100+100 points.

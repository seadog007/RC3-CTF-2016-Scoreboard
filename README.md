# RC3-CTF-2016-Scoreboard

## Basic Concept
Basically, the score is under the structure of a user  
So when I migrate a person who already solved the problem in the team to another team  
Then the score will be double for questions.  
Since the the limitation of each team is 5 users maximum, which can gives us 5 times of the original score. 

## PoC
Create `Account A`, `Account B`.  
`A`: Create `Team α`.  
`B`: Create `Team β`.  
`A`, `B` solved a question which is 100 points.  
`B` remove himself from the `β`, which also delete the team.  
`B` join the `α`.
Now, Team `α` has two people who already solved the question, so the team got 100+100 points.

## Example
I created 5 users, and created 5 team for each user.  
![Before](https://github.com/seadog007/RC3-CTF-2016-Scoreboard/raw/master/2016-11-19%2017_35_03-2016%20RC3%20Fall%20CTF.png)
  
Then let 5 users join the same team, the status of problem became  
![Before](https://github.com/seadog007/RC3-CTF-2016-Scoreboard/raw/master/2016-11-19%2017_40_31-2016%20RC3%20Fall%20CTF.png)

I solved some questions for each users, which gives me total 4500 points.  
![Scoreboard](https://github.com/seadog007/RC3-CTF-2016-Scoreboard/raw/master/2016-11-19%2017_38_03-2016%20RC3%20Fall%20CTF.png)

## Solution
1. Remove all submission after users leave a team
2. Check repeat submission, and remove them before a user join a new team

## Related Paper
[NIZKCTF: A Non-Interactive Zero-Knowledge Capture the Flag Platform](https://arxiv.org/abs/1708.05844)

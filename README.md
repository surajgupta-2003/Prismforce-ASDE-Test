# Abhimanyu's Journey through Chakravyuha
## Overview
This repository contains a C++ solution to a problem inspired by the Mahabharata, where Abhimanyu attempts to cross the Chakravyuha, a complex military formation. The goal is to navigate through 11 circles guarded by enemies, each with a specific power level, and determine if Abhimanyu can successfully cross all the circles.
This is me
## Problem Description
Circles and Enemies: There are 11 circles, each guarded by an enemy with a specified power.
Abhimanyu's Power: Abhimanyu starts with an initial power (p) and has the ability to skip battles (a skips) or recharge his power (b recharges).
Special Conditions:
Enemies in the 3rd and 7th circles regenerate with half their initial power if defeated.
If Abhimanyu's power is less than the enemy's power, he can skip the battle or recharge himself, depending on the availability of skips and recharges.
The challenge is to determine whether Abhimanyu can cross all 11 circles without losing all his power.

## Solution Approach
### Input Handling:
1.Read the power levels of enemies from the user. <br>
2.Read Abhimanyu's initial power, the number of skips, and the number of recharges available. <br>
### Simulation of Abhimanyu's Journey:
Iterate through each circle, managing Abhimanyu's power, skips, and recharges. For each enemy:<br>
1.Check if Abhimanyu can defeat the enemy with his current power , if he can then defeat the enemy and keep forward.<br>
2.Otherwise he will check for skip or refill himself depending upon the enemy power:<br>
  a)Check if after refilling he can defeat the enemy or not , if he cannot defeat the enemy even after refilling himself then if skip available use it otherwise he will LOSE.<br>
  b)Otherwise if refill available he will refill himself and attain his initial power and defeat the enemy if refill are not available then he will use skip ,if skip is also not 
  available he will LOSE. <br>
3.Special handling for the 3rd and 7th circles where enemies regenerate with half power.<br>
  Abhimanyu will use the same strategy to fight with them as discussed in 1. and 2.<br>
  

### Output:
The program outputs whether Abhimanyu can cross the Chakravyuha or not. <br>

### Test Cases and Their Outputs of my Code:
#### Test Case 1: <br>
Enter powers of enemies in 11 circles: 5 10 20 15 30 25 60 35 45 50 40 <br>
Enter Abhimanyu's initial power(p): 50 <br>
Enter the number of skips(a): 3 <br>
Enter the number of recharges:(b) 5 <br>
Abhimanyu can cross the Chakravyuha. <br>

#### Test Case 1: <br>
Enter powers of enemies in 11 circles: 5 10 20 15 30 25 60 35 45 50 40 <br>
Enter Abhimanyu's initial power(p): 50 <br>
Enter the number of skips(a): 2 <br>
Enter the number of recharges:(b) 5 <br>
Abhimanyu cannot cross the Chakravyuha. <br>




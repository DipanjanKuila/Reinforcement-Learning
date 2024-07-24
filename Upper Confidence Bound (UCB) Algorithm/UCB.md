# Upper Confidence Bound (UCB) Algorithm

The Upper Confidence Bound (UCB) algorithm is a method used in reinforcement learning to balance exploration and exploitation. It is particularly useful in scenarios where we need to choose between multiple options and want to maximize the reward over time. This README explains the steps involved in the UCB algorithm.

## Steps of the UCB Algorithm

### Step 1: Initialization
At each round \( n \), we consider two numbers for each ad \( i \):

- \( N_i(n) \): The number of times the ad \( i \) was selected up to round \( n \).
- \( R_i(n) \): The sum of rewards of the ad \( i \) up to round \( n \).

### Step 2: Calculation
From these two numbers, we compute:

The average reward of ad 
𝑖
i up to round 
𝑛
n:
𝑟
ˉ
𝑖
(
𝑛
)
=
𝑅
𝑖
(
𝑛
)
𝑁
𝑖
(
𝑛
)
r
ˉ
  
i
​
 (n)= 
N 
i
​
 (n)
R 
i
​
 (n)
​
 

The confidence interval for ad 
𝑖
i at round 
𝑛
n, denoted as:
Δ
𝑖
(
𝑛
)
=
3
log
⁡
(
𝑛
)
2
𝑁
𝑖
(
𝑛
)
Δ 
i
​
 (n)= 
2N 
i
​
 (n)
3log(n)
​
 
​


### Step 3: Selection
We select the ad \( i \) that has the maximum Upper Confidence Bound (UCB), which is calculated as:
\[ \text{UCB}_i(n) = \bar{r}_i(n) + \Delta_i(n) \]

This ensures that we balance exploration (trying out different ads) and exploitation (choosing the ad with the highest average reward).


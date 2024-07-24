# Upper Confidence Bound (UCB) Algorithm

The Upper Confidence Bound (UCB) algorithm is a method used in reinforcement learning to balance exploration and exploitation. This README explains the steps involved in the UCB algorithm.

## Steps of the UCB Algorithm

### Step 1: Initialization
At each round \( n \), we consider two numbers for each ad \( i \):

- \( N_i(n) \): The number of times the ad \( i \) was selected up to round \( n \).
- \( R_i(n) \): The sum of rewards of the ad \( i \) up to round \( n \).

### Step 2: Calculation
From these two numbers, we compute:

1. **The average reward of ad \( i \) up to round \( n \)**:
\[ \bar{r}_i(n) = \frac{R_i(n)}{N_i(n)} \]

2. **The confidence interval for ad \( i \) at round \( n \)**:
\[ \Delta_i(n) = \sqrt{\frac{3 \log(n)}{2 N_i(n)}} \]

### Step 3: Selection
We select the ad \( i \) that has the maximum Upper Confidence Bound (UCB), which is calculated as:
\[ \text{UCB}_i(n) = \bar{r}_i(n) + \Delta_i(n) \]

This ensures that we balance exploration (trying out different ads) and exploitation (choosing the ad with the highest average reward).



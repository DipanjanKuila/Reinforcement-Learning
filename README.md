# Reinforcement-Learning
# Upper Confidence Bound (UCB) Algorithm for Advertisement Selection

This project demonstrates the implementation of the Upper Confidence Bound (UCB) algorithm to solve the multi-armed bandit problem. The UCB algorithm is used in scenarios where you want to maximize the reward by balancing exploration (trying out different options) and exploitation (leveraging the best-known option).

## Table of Contents

1. [Installation](#installation)
2. [Dataset](#dataset)
3. [Algorithm Explanation](#algorithm-explanation)
4. [Code Explanation](#code-explanation)
5. [Results](#results)
6. [Conclusion](#conclusion)
7. [References](#references)

## Installation

To run this project, you'll need Python installed along with the following libraries:

- NumPy
- Matplotlib
- Pandas

You can install these libraries using pip:

```bash
pip install numpy matplotlib pandas

## Dataset
The dataset used in this project is a simulated dataset where each row represents a round, and each column represents an advertisement. The values indicate whether a user clicked on an advertisement (1) or not (0).

##Code Explanation
Here's a step-by-step explanation of the code:

### 1. Importing Libraries
We start by importing the necessary libraries, including NumPy for numerical operations, Matplotlib for plotting, and Pandas for handling the dataset.

### 2. Loading the Dataset
We load the dataset using Pandas. The dataset consists of rows representing rounds and columns representing different advertisements. Each cell in the dataset indicates whether a user clicked on the corresponding advertisement (1) or not (0).

### 3. Implementing UCB
We initialize the parameters and iterate over 10,000 rounds to apply the UCB algorithm.

N: Total number of rounds (10,000).
d: Number of ads (10).
ads_selected: Keeps track of the ads selected in each round.
numbers_of_selections: Stores the number of times each ad has been selected.
sums_of_rewards: Stores the total reward of each ad.
total_reward: Stores the total accumulated reward.
For each round:

We calculate the UCB for each ad.
We select the ad with the highest UCB.
We update the number of selections and the sum of rewards for the selected ad.
We accumulate the total reward.
4. Visualizing the Results
We plot a histogram to visualize the number of times each ad was selected. This helps in understanding the distribution of ad selections, indicating which ads were explored and exploited more frequently by the UCB algorithm.

### Results
The results show the distribution of ad selections. The histogram indicates the number of times each ad was selected, providing insights into how the UCB algorithm balances exploration and exploitation.

## Conclusion
The UCB algorithm effectively balances exploration and exploitation, ensuring that the best-performing ads are selected more frequently over time. This approach is beneficial in scenarios where you want to maximize rewards while still exploring new options.

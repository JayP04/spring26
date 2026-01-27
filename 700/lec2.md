# Reinforcement learning

## why reinforcement learning?
- sequential decision making problems 
    - ex: playing chess, driving a car, managing inventory
    - observation of state -> action -> reward -> new observation
    - for observation of state, its not jjust an image, if used radar to understand the surroundings, we provide reward based on how well the action was executed (postivie or negative)
- for LLM, the prompt is state, the output is action, and reward is based on how well the output aligns with human preference
- your loss function objective is 
    - in some cases your objective is not differentiable
    - in other way it can be used to optimize long term reward - reward is based on your opiniion, rl has its own optimization strategy. 
- It can be taken as another, just like gradient descent, to optimize your model
### Benefits of RL
- dont need to extract feature one by one, use NN to make it super fast.
- in stanadar way we extact feature, low level, then middle level so one by one.
- but in ened to end - > input raw data, output action. its very easy to scale up.
- we dont care, min, ro stuff, just provide model structure and reward, model will learn by itself
- rl at an intial state, its in tabular state - in tabular state, we have a table of states and actions, and we update the table based on reward
- deep rl can handle more state action pairs, more complex scenarios
### Can be used in various fields
- rl can be integrated with Artificial NN
- can be used to manipulate 

## Probability things

###
- a variable whose possible values are numerical outcomes of a random phenomenon
- can be discrete or continuous
- discrete random variable - finite or countable outcomes
    - ex: rolling a dice, number of heads in coin toss
- continuous random variable - infinite outcomes within a range
    - ex: height, weight, temperature

### Probability Density Function (PDF)
- function that describes the likelihood of a random variable to take on a particular value
- for exampel , gaussian distribution
    - mean = 0, variance = 1

### Probability Mass Function (PMF)
- function that gives the probability that a discrete random variable is exactly equal to some value
- for example, rolling a fair six-sided dice

## Terminologies in RL
- state (s) - representation of the environment at a specific time
- action (a) - decision or move made by the agent
- policy (π) - strategy that the agent employs to determine actions based on states 
    - policy is simply the probabilty of taking an action is taken given a specific state.
    - random vs deterministic policy
        - random - gives a probability distribution over actions for each state. It can help us increase the exploration of the environment and subotimal actions.
        - deterministic - maps each state to a specific action
- reward (r) - feedback signal indicating the immediate benefit of an action taken in a particular state
- state transition - movement from one state to another as a result of an action
- Agent - Environment interaction
    - agent takes action based on current state
    - environment responds with new state and reward
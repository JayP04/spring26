## Continuing DQN
- its a neural network
- parametirized by weight W.
- we select the action that can maximize the future reward. 

## TD 
- temporal differnece 
- an agent observes state st, takes action at, receives reward rt and next state st+1
- the environment provides that new state and reward
- td target = rt + gamma * max_a' Q(st+1, a'; W)
- td error
- goal is to minimize the qt close to yt for all t. 
- loss function: mean squared td error
- we try to minimize the loss function by changing the weights L(w)
- we use stochastic gradient descent to minimize the loss function
- online gradient descent 
    - we discard the data after one update
    - so its only used once. 

### problems with correlated updates
- 2 shortcoimings
    - correlated states
    - 

### to overcome these problems
- experience replay
    - we store the recent experiences in a replay buffer
    - we think the most recent experiences are the most relevant and importnat
- Benefits
    - udpates the correlated states
    - resuse the collected experiences multiple times
    
### integration of TD with experience replay
- we have buffer, we  randomlly sample the transitions from the buffer to compute the td error and update the weights

### prioritzed experience replay
- not all transitions are equally useful for learning
- we can prioritize the transitions with high td error
- we choose classification of transitions based on td error
- importance sampling
    - the sampling probablity is chance to importnace sampling instead of unform sampling. 

### scaling learning rate
- high importance transition have low leraning rates
- 1/(np_t)^beta


## bottstrappiing in reinformcement learning
- 
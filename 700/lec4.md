# Action based value

## Discounted Return Q(s,a)
- action value function for policy
    - we integrate till we are left with St and At
- optimal action value function

## Deep Q learning
- goal is to win the game i.e maximize the total reward
- Question: if we konw Q*(s,a) what is the best action? 
    - A: take action that maximizes Q*(s,a). So the optimal policy is 
        - a* = argmax_a Q*(s,a)
- Challenge is that we dont Q*(st,at)
- solution: deep q learning

## DQN
- input shape and output shape
    - input shape: state representation (for ex: in atari game, its the image frames)
    - output shape: q values for each possible action in that state
- input shape - size of screenshot -> conv layers -> feature(flatten) -> dense layers -> output layer (q values for each action)

- image classification - we use soft max to activate the last layer
- dqn - we want q values, so no activation function in the last layer

- optimization is the most challenging part in both dqn and rl in general
- different optimization defines different rl algorithms

### apply dqn to play game
- from state to an action 
    - at = argmax_a Q(st,a;w)
- from a_t action we have 


## Temporal Differnce (TD) Learning
- 
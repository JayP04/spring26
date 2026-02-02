## Why does overestimation happen?
- DQN Estimates action-Value Function Using the Maximum Action Value as an Approximation of the Optimal Action Value
- the TD target is an overestimate of the true optimal action value
- the bootstrapping propogates the overstimatino back to the current estimate
- the maximization leads to overestimation bias
- the TD target is a worse overestimation
- and then the bootstratiping that goes back ames the DQN make worse overestimation

### Why is overestiation harmful?
- assume we have a state and that is being given to a DQN.
- the DQN wil provide the action values for all the actions in that state.
- the gent is controlled by DQN 
- if uniformtaion overstimation happens, its not a problem.
- if non uniform, then there is a possibility that the agent will choose an action which could be the worst one.
- so non uniform overestimation is harmful

## solution
- we can use a target network 
- double DQN to limit the overestimation bias


## Double DQN

### native update
- we use the online network to select the action that maximizes the action value in the next state
    - selection using DQN
        - a* = argmax_a' Q(st+1, a'; W)
    - evalutaiton using target network 
        - if we use this, we can limit the overestimation bias
[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"



## Environment Overview

This uses Unity's [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

![Trained Agent][image1]

(the image above has multiple robot arms, but in this repository, only one robot arm is implemented)

#### Conditions

A double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

#### Reward
- +0.1 hit the ball over the net 
- -0.01 let the ball hit the ground
- -0.01 let the ball hit out of bounds
- The score is rewarded to both players

#### State Space

- Continuous 8 dimensions
- They correspond to:
    - positions
    - velocities
    - above for the ball and the racket
- Each player observes independently

#### Action Space
- Continuous 2 dimensions (movement toward net, jumping)
    - Each player takes actions independently 
    - Each has range of [-1, 1]

####  Goal of the agent 

- get an average episode score of more than +5  
- the look back period to calculate the average is 100 consecutive eposodes 

<hr>

## Used Algorithm 



#### Performance

- 




#### Ideas for Future Work

- Architecture: Currently, just used simple NN. Going forward, using more complex architecture may improve the score
- Hyperparameter: the parameter has not been fully optimized. Here is another opportunity of improvement


<hr>

## How to Run

- The trained model is `checkpoint.pth`. You can use this on Unity environment


#### Dependencies

1. Download the Unity environment from one of the links below
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    

2. Place the file in this repository and unzip 

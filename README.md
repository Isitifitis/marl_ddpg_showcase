[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"


## Introduction

In this project, we train a competing agents in a Tennis environment to try and bounce a ball back and forth over the net for as long as possible. We train both of the agents using the DDPG algorithm, which is described in the [report](Report.md).

![Trained Agent][image1]

### Environment

The task is episodic, and in order to solve the environment, the agent should get an average score of +0.5 over 100 consecutive episodes.

#### Reward

A reward of +0.1 is provided for time an agent hits the ball over the net, while -0.01 is the reward for dropping the ball or hitting it out of bounds. 

Thus, the goal of the agents is to continue playing for as many time steps as possible.
#### States

The state space has 24 variables, 8 for each of the agents and the ball, corresponding to position and velocity.
#### Actions

Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

Every entry in the action vector should be a number between -1 and 1.
### Environment Setup

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

2. Place the file in this project's root, and unzip (or decompress) the file.

3. Install the needed python packages (Best to create a [virtual environment](https://virtualenv.pypa.io/en/latest/) to contain them first!)

```
pip install -r requirements.txt
```

### Training

Run the cells in the notebook [Training.ipynb](Training.ipynb) in order to train the agent. If it reaches the threshold set in the `train_agent` function, then it will save the model weights for (agents 1 & 2) in `first_score_critic_model.pth` and `first_score_actor_model.pth`.

### Report

Additional details about the implementation of the algorithm can be found in [Report.md](Report.md).

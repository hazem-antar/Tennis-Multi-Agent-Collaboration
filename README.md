# Udacity Deep Reinforcement Learning Nanodegree
## Project 3 - Collaboration and Competition

This project is the third and final in Udacity's Deep Reinforcement Learning Nanodegree. In this project, the goal is to implement multiagent model/s based on [Deep Deterministic Policy Gradient (DDPG)](https://arxiv.org/abs/1509.02971) to play Tennis with each other in a Unity ML-Agents environment.


![Trained DQN Agent](./img/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif)


## Environment description

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.


## Task description

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,
•	After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
•	This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.


## Dependencies Installation and Usage Guide

1. Prepare new Conda environment (with python 3.6) following guidelines on [Udacity DRL repo](https://github.com/udacity/deep-reinforcement-learning#dependencies) 

2. Install the `unityagents` package with:

```sh
pip install unityagents==0.4.0
```

3. Download the environment from one of the links below.  You need only select the environment that matches your operating system:

      - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
      - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
      - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
      - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    

4. Place the downloaded zip file in the root directory of this repository and unzip it.

5. Path to the executable file has to be provided to `UnityEnvironment` function in `Tennis.ipynb` 

      For example on 64-bit Windows:
      ```python
      env = UnityEnvironment(file_name='./Tennis_Windows_x86_64/Tennis.exe')
      ```

4. Run the `Tennis.ipynb` notebook to either train the DDPG agent from scratch or use the already trained model weights in the files `checkpoint_actor.pth` and `checkpoint_critic.pth`.

5. Watch a smart agent playing!

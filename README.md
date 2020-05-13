# Reacher_Continuous_Control
Reacher Continuous Control using DDPG
### Reacher Enviroment
![Reacher](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/reacher.gif)

## 1. Environment

Note that your project submission need only solve one of the two versions of the environment 1 agent and 20 agents

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:

    - **_Version 1: One (1) Agent_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

    - **_Version 2: Twenty (20) Agents_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

#### Option 1: Solve the First Version

The task is episodic, and in order to solve the environment,  your agent must get an average score of +30 over 100 consecutive episodes.


![One Reacher](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/one_agent.png)


- ***Observations***: Each agent receives an observation consisting of a 33-dimensional vector with measurements like relative position and orientations of the links, relative position of the goal and its speed, etc..

![Obseravations](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/img_reacher_environment_observations.png)

- ***Actions***: Each agent moves its arm around by applying actions consisting of 4 torques applied to each of the 2 actuated joints (2 torques per joint).

![Actions](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/img_reacher_environment_actions.png)

- ***Rewards***: Each agent gets a reward of +0.1 each step its end effector is within the limits of the goal. The environment is considered solved once the agent gets an average reward of +30 over 100 episodes.



#### Option 2: Solve the Second Version

The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents.  In particular, your agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).  Specifically,
- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent.  This yields 20 (potentially different) scores.  We then take the average of these 20 scores. 
- This yields an **average score** for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. 

## 2. Solve the First Version Reacher One Arm
In this version we use Deep Deterministic Policy Gradient (DDPG) to solve problem.

- DDPG is an off-policy algorithm.
- DDPG can only be used for environments with continuous action spaces.
- DDPG can be thought of as being deep Q-learning for continuous action spaces.
- The Spinning Up implementation of DDPG does not support parallelization.


# References



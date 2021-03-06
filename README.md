# Reacher_Continuous_Control
Reacher Continuous Control using DDPG
### Reacher Enviroment
![Reacher](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/reacher.gif)

## 1. Setup Environment and Install Requirements 
The Project use the MLAngents version 0.4.0 so we need to do some following steps
### 1.1 Install Anaconda & Create virtual environment using conda
Install Anaconda following link bellow

https://www.anaconda.com/products/individual

Create virtual environment

```
# Create the virtual env DQN
conda create -n DQN_navigation python=3.6
# activate environment
source activate DQN_navigation
```
### 1.2 Install all dependence
```

# clone the udacity repo
git clone https://github.com/udacity/deep-reinforcement-learning.git

# go to the python folder of the repo
cd deep-reinforcement-learning/python

# install the unityagents package from this folder
pip install -e .

# git clone DQN_Navigation_Project
cd ..
https://github.com/TriKnight/Reacher_Continuous_Control

# install the requirements from our package
cd Reacher_Continuous_Control
pip install -r requirements.txt

```
### 1.3 Create and Adding Kernel to Jupyter notebook
```
conda install -c anaconda ipykernel
python -m ipykernel install  --user --name=DQN_navigation
```
1. Open Jupyter notebok. 
```
jupyter notebook
```
2. Open Reacher_Continuous_Control


3. Change the Kernel ```Kernel/Change Kernel/DQN_navigation```



## 2. Environment

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

## 3. DDPG Algorithms
![DDPG Algorithms](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/DDPG%20Algorithms.png)
## 4. Solve the First Version Reacher One Arm
In this version we use Deep Deterministic Policy Gradient (DDPG) to solve problem.

- DDPG is an off-policy algorithm.
- DDPG can only be used for environments with continuous action spaces.
- DDPG can be thought of as being deep Q-learning for continuous action spaces.
- The Spinning Up implementation of DDPG does not support parallelization.

The Neural network of the Actor-Critic
![Actor-Critic Network](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/actor_critic_networks.png)

# References
-  [CONTROL  WITH  DEEP  REINFORCEMENTLEARNING](https://arxiv.org/pdf/1509.02971.pdf)
-  [Reproducibility of Benchmarked DRL Tasks for Continuous Control](https://arxiv.org/pdf/1708.04133.pdf)
-  [Parameter Noise](https://openai.com/blog/better-exploration-with-parameter-noise/)
-  [Open AI DDPG Algorithms](https://spinningup.openai.com/en/latest/algorithms/ddpg.html#id7)
-  [Wpumacay Blog](https://wpumacay.github.io/projects.html)
-  [Silviomori Blog](https://github.com/silviomori/udacity-deep-reinforcement-learning-p2-continuous-control)




# Reacher_Continuous_Control
Reacher Continuous Control using DDPG
### Reacher Enviroment
![Reacher](https://github.com/TriKnight/Reacher_Continuous_Control/blob/master/misc/reacher.gif)

### Solving the Environment

Note that your project submission need only solve one of the two versions of the environment.
Option 1: Solve the First Version

The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.
Option 2: Solve the Second Version

The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, your agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically,

    After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
    This yields an average score for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30.

# Reacher_Continuous_Control
Reacher Continuous Control using DDPG
### Reacher Enviroment

    Set-up: Double-jointed arm which can move to target locations.
    Goal: The agents must move its hand to the goal location, and keep it there.
    Agents: The environment contains 10 agent with same Behavior Parameters.
    Agent Reward Function (independent):
        +0.1 Each step agent's hand is in goal location.
    Behavior Parameters:
        Vector Observation space: 26 variables corresponding to position, rotation, velocity, and angular velocities of the two arm rigid bodies.
        Vector Action space: (Continuous) Size of 4, corresponding to torque applicable to two joints.
        Visual Observations: None.
    Float Properties: Five
        goal_size: radius of the goal zone
            Default: 5
            Recommended Minimum: 1
            Recommended Maximum: 10
        goal_speed: speed of the goal zone around the arm (in radians)
            Default: 1
            Recommended Minimum: 0.2
            Recommended Maximum: 4
        gravity
            Default: 9.81
            Recommended Minimum: 4
            Recommended Maximum: 20
        deviation: Magnitude of sinusoidal (cosine) deviation of the goal along the vertical dimension
            Default: 0
            Recommended Minimum: 0
            Recommended Maximum: 5
        deviation_freq: Frequency of the cosine deviation of the goal along the vertical dimension
            Default: 0
            Recommended Minimum: 0
            Recommended Maximum: 3
    Benchmark Mean Reward: 30

# Continuous-Control-Deep-RL

## Environment Details

In the environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

## Dependencies

To run the code and train the agent, the dependencies in the ./python folder need to be installed via the command

```
!pip -q install ./python
```

The command, however, is also included into the solution notebook.


Also, the UnityEnvironment package needs to be installed. Detailed instructions can be found here (https://classroom.udacity.com/nanodegrees/nd893/parts/286e7d2c-e00c-4146-a5f2-a490e0f23eda/modules/089d6d51-cae8-4d4b-84c6-9bbe58b8b869/lessons/5b822b1d-5c89-4fd5-9b52-a02ddcfd3385/concepts/2303cf3b-d5dc-42b0-8d15-e379fa76c6d5 "here").

## Instructions

The code can be run via the provided "Solutions.ipynb" notebook. The notebook is built consecutively, thus running all cells via the _Cell->Run All_ command will train the agent and display the results.

Note: If the agent should act solely based on the learned weights, it is required though to change the epsilon value to a value close to 0 in order to disable the epsilon-greedy policy accordingly.

## Further files

The trained weights are saved in the "checkpoint.pth" as a PyTorch state dictionary. In order to load the trained weights and continue training based on those weights, the _retrain_ hyperparameter needs to be set to _True_.

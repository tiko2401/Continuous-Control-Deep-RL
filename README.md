# Continuous-Control-Deep-RL

## Environment Details

The environment is a continuous space within the Banana Collection environment provided bei UnityEnvironment. 
There is one Agent acting in the environment. 
The action space is __discrete__ and consists of four actions, namely 0 (forward), 1(backward), 2(left), 3(right) which the agent can use to navigate through the environment.
The Agent acts based on a state it receives as input. The __state space__ has 37 dimensions which represent the state e.g. in terms of its velocity.
As the Agent navigates through the environment, it receives rewards for collecting bananas. For yellow bananas the reward is +1, for blue ones it is -1. 
The environment is considered closed when the Agent collected __a reward of +13__ over 100 consecutive episodes.

## Dependencies

To run the code and train the agent, the dependencies in the ./python folder need to be installed via the command

```
!pip -q install ./python
```

The command, however, is also included into the solution notebook.


Also, the UnityEnvironment package needs to be installed. Detailed instructions can be found here (https://classroom.udacity.com/nanodegrees/nd893/parts/6b0c03a7-6667-4fcf-a9ed-dd41a2f76485/modules/4eeb16ab-5ac5-47bf-974d-12784e9730d7/lessons/69bd42c6-b70e-4866-9764-9bfa8c03cdea/concepts/319dc918-bd2c-4d3b-80a5-063bb5f1905a "here").

## Instructions

The code can be run via the provided "Solutions.ipynb" notebook. The notebook is built consecutively, thus running all cells via the _Cell->Run All_ command will train the agent and display the results.

Note: If the agent should act solely based on the learned weights, it is required though to change the epsilon value to a value close to 0 in order to disable the epsilon-greedy policy accordingly.

## Further files

The trained weights are saved in the "checkpoint.pth" as a PyTorch state dictionary. In order to load the trained weights and continue training based on those weights, the _retrain_ hyperparameter needs to be set to _True_.

# Reacher_AIGym_Continuous-Control
Solving the AI Gym's Reacher environment with DDPG (Deep Deterministic Policy Gradient) implementation

This project is an implementation of AI Gym's [environment](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher)


![](agents.gif)

## Project description

In this environment called Reacher, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal the agent is to maintain its position at the target location for as many time steps as possible.

- Actions: Vector Action space: (Continuous) Size of 4, corresponding to torque applicable to two joints.

- Spaces: The observation space is composed of 33 variables: position, rotation, velocity, and angular velocities of the arm.

- Rewards: A reward of +0.1 is provided for each step that each agent's hand is in the goal location independently.

- Solution criteria: The environment is considered solved when the average mean score of all agents reach 30+ in the last 100 epsisodes.

- Goal: The goal is to control the 20 arms to move to their individual target locations and keep them there as many time steps as possible.

## Installation

1. Download the environment from one of the links below. You need to select only the environment for your operating system:

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
(For Windows users) Check out this [link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not enabled a [virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use this [link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the DRLND GitHub repository, in the root folder, and unzip (or decompress) the file.

3. Make sure you install Anaconda. You can download it from [here](https://www.anaconda.com/distribution/)

4. Now you can create your environment. Lets call our environment ```DRLND```
  
   Linux,Mac
   ```
   conda create --name drlnd python=3.6
   source activate drlnd
   ```
   Windows
   ```
   conda create --name drlnd python=3.6 
   activate drlnd
   ```
 5. We will be working with pytorch version 0.4.0 (an early version), so make sure that you install this version of pytorch:
   ```
   conda install pytorch=0.4.0 -c pytorch
   ```
 6. Perform a minimal installation of the [OpenAI Gym environment](https://github.com/openai/gym)
 
 7. Use command ```pip install``` and use it with all dependencies of the requirements.txt file
 
 8. Create a Python execution backend for Jupyter for the drlnd environment 
   ```
   python -m ipykernel install --user --name drlnd --display-name "drlnd"
   ```
 AND you are ready to use the environments

## Instructions
Follow the instructions in ```Continuous_Control.ipynb``` to get started with training your own agent! **For this implementation solution with 20 agents was used.**

## Run the code
Execute the cells inside ```Continuous_Control.ipynb``` file in sequential order so to proceed with training the agents. Tweak the hyperparameters to get different results. Using GPU gives 4 times faster results.

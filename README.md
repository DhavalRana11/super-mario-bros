 
gym-super-mario-bros:

This is a private project to make Super Mario Agent.
It consists of training an agent to clear Super Mario Bros with deep reinforcement learning methods.
Here are my super mario agents with dueling network.

 
The preferred installation of gym-super-mario-bros is from pip:
pip install gym-super-mario-bros

 
 Install Requirements
 pip install -r requirements.txt

 
 Python:
 You must import gym_super_mario_bros before trying to make an environment. This is because gym environments are
 registered at runtime. By default, gym_super_mario_bros environments use the full NES action space of 256 discrete
 actions. To contstrain this, gym_super_mario_bros.actions provides three actions lists (SIMPLE_MOVEMENT,
 and RIGHT_ONLY) for the nes_py.wrappers.JoypadSpace wrapper. See gym_super_mario_bros/actions.py for 
 A breakdown of the legal actions in each of these three lists.


process the Enviroment
Install Dependencies: 
import os
from nes_py.wrappers import JoypadSpace
import gym 
import gym_super_mario_bros
from gym_super_mario_bros.actions import SIMPLE_MOVEMENT, RIGHT_ONLY 


process the Enviroment:
env = gym_super_mario_bros.make('SuperMarioBros-1-1-v0')
env = JoypadSpace(env, SIMPLE_MOVEMENT)


Test the Env_wrap:
done = True
for i in range(150):
    if done:
        state = env_wrap.reset()
    state, reward, done, info = env_wrap.step(env_wrap.action_space.sample())


Setup the Reinfocements learning Model:
MODIFY THESE TWO DIRECTORIES BEFORE TRAINING A NEW MODEL
that's means location of file in your device  


Train the model:
counting time  
               fps            
               iterations     
               time_elapsed   
               total_timesteps


save and load trained model :
using location path://


Test the trained model:

 Result:
 score.p : save total score every 50 episode
.pth : save weight of q, q_target every 50 training
 
Evaluate:
Now, pre-trained agent has been corrupted
Test and render trained agent.
To test our agent, we need 'q_target.pth' that generated at the training step.

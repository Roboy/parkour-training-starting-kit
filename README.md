# Roboy Parkour Challenge training starter kit

This repo contains most of the stuff you need to implement to begin training your model for Roboy Parkour Challenge (if you decide to try the reinforcement learning solution, of course. Go directly for classical ZMP if you like!)

## Installing prerequisites

We use OpenAI Gym, PyBullet and PyBullet Gymperium for the training. 

You can install everything like this:

```bash
pip install pybullet

git clone https://github.com/openai/gym.git
cd gym
pip install -e .

git clone https://github.com/benelot/pybullet-gym.git
cd pybullet-gym
pip install -e .
```



## Implementation details
An example of a robot acceptable by the challenge is implemented and can be tested by running ```example.py``` Your robot class should implement the abstract class in ```gym_parkour/envs/parkour_robot.py```. 

We highly suggest using URDF-based robots as can be seen in the example, to allow for an easy deployment using ROS/Gazebo which may be required from you during the challenge. 

If you want to try out our pre-made robot, you can implement ```ReactivePolicy``` from our example. You may also want to change the contents of the main loop in the example to use the reward(you might want to reimplement them in ```calc_reward(...)``` located in ```gym_parkour/envs/parkour_gym.py```)  and observations (implementation is up to you) of a training episode for your learning. 

We recommend reading the OpenAI Gym documentation to clarify any questions:
http://gym.openai.com/docs/
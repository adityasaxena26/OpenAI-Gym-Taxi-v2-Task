# Deep Learning Nanodegree
## Reinforcement Learning
## Project: OpenAI-Gym-Taxi-v2-Task

Use OpenAI Gym's Taxi-v2 environment to design an algorithm to teach a taxi agent to navigate a small gridworld.

### The Taxi Problem:
There are four designated locations in the grid world indicated by R(ed), B(lue), G(reen), and Y(ellow). When the episode starts, the taxi starts off at a random square and the passenger is at a random location. The taxi drive to the passenger's location, pick up the passenger, drive to the passenger's destination(another one of the four specified locations), and then drop off the passenger. Once the passenger is dropped off, the episode ends.

### Observations:

There are 500 discrete states since there are 25 taxi positions, 5 possible locations of the passenger (including the case when the passenger is the taxi), and 4 destination locations.

### Actions:

There are 6 discrete deterministic actions:
- 0: move south
- 1: move north
- 2: move east
- 3: move west
- 4: pickup passenger
- 5: dropoff passenger

### Rewards:

There is a reward of -1 for each action and an additional reward of +20 for delievering the passenger. There is a reward of -10
for executing actions "pickup" and "dropoff" illegally.
Rendering:
- blue: passenger
- magenta: destination
- yellow: empty taxi
- green: full taxi
- other letters (R, G, B and Y): locations for passengers and destinations
actions:
- 0: south
- 1: north
- 2: east
- 3: west
- 4: pickup
- 5: dropoff

state space is represented by:
(taxi_row, taxi_col, passenger_location, destination)


### Project Instructions

Clone the repository and navigate to the downloaded folder.
```
git clone https://github.com/adityasaxena26/OpenAI-Gym-Taxi-v2-Task.git
cd OpenAI-Gym-Taxi-v2-Task
```

The project contains these files:

```agent.py```: Develop your reinforcement learning agent here. This is the only file that you should modify.

```monitor.py```: The interact function tests how well your agent learns from interaction with the environment.

```main.py```: Run this file in the terminal to check the performance of your agent.

```taxi.py```: OpenAI Gym environment implementation from [here](https://github.com/openai/gym/blob/master/gym/envs/toy_text/taxi.py).

Open all of these files in the terminal.

run ```main.py``` by executing ```python main.py``` in the terminal.

When you run ```main.py```, the agent that you specify in ```agent.py``` interacts with the environment for 20,000 episodes. The details of the interaction are specified in ```monitor.py```, which returns two variables: ```avg_rewards``` and ```best_avg_reward.```

```avg_rewards``` is a deque where ```avg_rewards[i]``` is the average (undiscounted) return collected by the agent from episodes i+1 to episode i+100, inclusive. So, for instance, ```avg_rewards[0]``` is the average return collected by the agent over the first 100 episodes.

```best_avg_reward``` is the largest entry in ```avg_rewards```. This is the final score that you should use when determining how well your agent performed in the task.

### Evaluate your Performance
You can modify the ```agents.py``` file to improve the agent's performance.

OpenAI Gym defines "solving" this task as getting average return of 9.7 over 100 consecutive trials.

### Softwares Prerequisites:
* Python 3.5+
* Jupyter Notebook

While Jupyter runs code in many programming languages, Python is a requirement (Python 3.3 or greater) for installing the Jupyter Notebook.

For new users, installing Anaconda is highly recommended. Anaconda conveniently installs Python, the Jupyter Notebook, and other commonly used packages for scientific computing and data science.
As an existing Python user, you may wish to install Jupyter using Python’s package manager, ```pip```, instead of Anaconda.

First, ensure that you have the latest pip; older versions may have trouble with some dependencies: ```pip3 install --upgrade pip```

Then install the Jupyter Notebook using:
```pip3 install jupyter```

To run the notebook:
``` jupyter notebook```
* OpenAI Gym
To get started, you’ll need to have Python 3.5+ installed. Simply install gym using pip:

```pip install gym```

The following packages (libraries) need to be installed. You can install these packages via conda or pip.
* NumPy

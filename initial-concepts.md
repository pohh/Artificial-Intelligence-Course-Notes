# Initial Concepts

## Definitions
There are many definitions for AI. Most of them can be divided into four groups:

* thinking like a human: use of models representing the inner mechanisms of human mind (related to **cognitive science**);
* acting like a human: passing on [Turing Test](https://en.wikipedia.org/wiki/Turing_test);
* thinking rationally: use of **logic**;
* acting rationally: use of rational agents that do the “right thing”.

AI, as a subfield of CS, is more related to the last definition. As Peter Norvig puts it, *“AI is programming a computer to do the right thing when you don’t know for sure what the right thing is”*.

## Main disciplines
* Natural language processing
* Knowledge representation
* Automated reasoning
* Machine learning
* Computer vision
* Robotics

## Intelligent agents
An agent is anything surrounded by an environment and capable of (1) **sense** the environment and (2) **act** upon it. The actions of an agent are dependent of the percepts he receives. The mapping of percepts and actions is called **agent function**. An agent function can be implemented through an **agent program** running on some **architecture**.

An rational agent is one that acts the best way possible, according to some **performance measure**. This measure should be dependent on the environment states generated by the agent’s actions and not on what the agent internally perceives as a good result.

The rationality of an agent is conditional to (1) the performance measure, (2) the environment, (3) the agent’s actuators and (4) the agent’s sensors.

In order to perform well in more complex environments, a rational agent should be autonomous, learning as time pass by to compensate for partial or incorrect prior knowledge.

## Environments
Environment is the set of things that an agent can get its percepts from and where the agent’s actions may change its state. An environment can be:
* With respect to the “observality”:
    * **Fully observable**, when the agent can sense the complete state of the environment, and consequently doesn’t need to maintain any internal state to keep track of the world.
    * **Partially observable**, when the agent can sense only a part of the environment.
    * **Unobservable**, when the agent has no sensors at all.
* With respect to the number of agents in it, **single agent** or **multiagent**.
* With respect to the dynamics of state changing *in response to actions*:
    * **Deterministic**, when its next state is completely determined by the current state and the agent’s action.
    * **Stochastic**, when otherwise.
* With respect to the dynamics of state changing *with the passage of time*:
    * **Static**, when its state only changes in response to agent’s actions.
    * **Dynamic**, otherwise. As a special case, we call **semidynamic** an environment that doesn’t change its states by itself with time, but changes the agent’s performance score (e.g. chess played with clock).
* With respect to the influence of past agent’s actions on its state:
    * **Episodic**, when the agent’s past actions don’t influence its next state. Only the current action is taken into account.
    * **Sequential**, when the sequence of the agent’s past actions influences its future states.
* With respect to the knowledge of its future states:
    * **Known**, when it’s previously known what state will be obtained for all possible actions.
    * **Unknown**, when otherwise.

## Types of agents
Agents may have different types depending on how its program is made. The main types of agents are:
* **Simple reflex agents**: the ones who select actions on the bases of the current percept, ignoring any past percepts. The program of such agents are mainly composed of simple if-then rules. These agents only perform well on fully observable environments.
* **Model-based reflex agents**: the ones who maintain an internal state to keep track of the environment. This allows those agents to deal with partially observable environments. They have a model of what happens to the environment for each given action so, after every action, they update their internal state.
* **Goal-based agents**: the ones who have, in addition to the model-based reflex agent capabilities, a model to check if a particular environment state is helpful or not for it to achieve some goal. These agents will take actions that produce environment states that are helpful to their goals.
* **Utility-based agents**: similar to goal-based agents, utility-based agents also consider if a particular environment state is helpful or not to achieve a goal, but they do that using a utility function which can account for multiple (sometimes conflicting) goals. These agents will take actions that maximize their expected utility outcomes.
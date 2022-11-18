## Exersice solutions for Chapter 2 - Intelligent Agents


### 2.1
**Q:** 
Suppose that the performance measure is concerned with just the first *T* time steps of the environment and ignores everything thereafter. Show that a rational agent’s action may depend not just on the state of the environment but also on the time step it has reached.

**A:** 
If our agent is, say, a smarty home-grade coffee machine, the environment may tell it to make a long espresso, but the time step, being the number of coffees it has made in its life, tells it that it needs to start a self-cleaning program. An agent that ignores time steps can hardly be intelligent in such cases.

### 2.2 
**Q:** 
Let us examine the rationality of various vacuum-cleaner agent functions.
*a.* Show that the simple vacuum-cleaner agent function described in Figure 2.3 is indeed rational under the assumptions listed on page 38.
*b.* Describe a rational agent function for the case in which each movement costs one point. Does the corresponding agent program require internal state?
*c.* Discuss possible agent designs for the cases in which clean squares can become dirty and the geography of the environment is unknown. Does it make sense for the agent to learn from its experience in these cases? If so, what should it learn? If not, why not?

**A:**
*a:* If the agent was not rational, then it would not be trying to maximize its performance measure, being the floor has to be clean. That means that it would leave dirt on the floor when it sees it or would not try to update its information about the environment whenever it can. Both of these are incorrect when looking at the agent function as it does everything it can to clean the floor.
*b:* Even if it has internal state, the agent has to update its state frequently as it can not be sure whether the other location is clean unless it visits it. If it has internal state that would stop the agent from constantly switching between the locations which can be wasteful. However if the agent stays at the same spot it loses the chance to clear the neighbouring location and thus misses points. I think it would be optimal to have state and occasionally switching location to check whether it is clean. That is all in the case that a clean square can become dirty.
*c:* 


### 2.3 
**Q:** 
For each of the following assertions, say whether it is true or false and support your answer with examples or counterexamples where appropriate.
*a.* An agent that senses only partial information about the state cannot be perfectly rational.
*b.* There exist task environments in which no pure reflex agent can behave rationally.
*c.* There exists a task environment in which every agent is rational.
*d.* The input to an agent program is the same as the input to the agent function.
*e.* Every agent function is implementable by some program/machine combination.
*f.* Suppose an agent selects its action uniformly at random from the set of possible actions. There exists a deterministic task environment in which this agent is rational.
*g.* It is possible for a given agent to be perfectly rational in two distinct task environments.
*h.* Every agent is rational in an unobservable environment.
*i.* A perfectly rational poker-playing agent never loses.

**A:**
*a:* False, it can choose the most optimal action given all the possibilities that arise from the sensations. For example are blind people not rational?
*b:* Sure, all environments with infinite state spaces.
*c:* Some trivial environment with no sensors or actuators
*d:* Not always true, the program implementation can be more complex than the mathematical function


### 2.4 
**Q:** 
For each of the following activities, give a PEAS description of the task environment and characterize it in terms of the properties listed in Section 2.3.2.
*a.* Playing soccer.
*b.* Exploring the subsurface oceans of Titan.
*c.* Shopping for used AI books on the Internet.
*d.* Playing a tennis match.
*e.* Practicing tennis against a wall.
*f.* Performing a high jump.
*g.* Knitting a sweater.
*h.* Bidding on an item at an auction.

**A:**
*a.* 
* performance measure - playing fair, not making fails, guarding your goal and scoring goals;
* environment - the stadium, all players in the game, the ball and the referee;
* actuators - your full body;
* sensors - all human senses
* it is fully observable, multi-agent, deterministic, sequential, dynamic, continuous, known

*b:* 
* performance measure - seeing as much as possible without dying
* environment - the submarine and everything in the ocean including the properties of the moon
* actuators - everything the submarine can do
* sensors - everything the ship can sense
* it is partially observable(as it is unknown), single-agent(possibly multi), nondeterministic, sequential, dynamic, continuous and unknown


### 2.5 
**Q:** 
Define in your own words the following terms: agent, agent function, agent program, rationality, autonomy, reflex agent, model-based agent, goal-based agent, utility-based agent, learning agent.

**A:**

### 2.6 
**Q:** 
This exercise explores the differences between agent functions and agent programs.
*a.* Can there be more than one agent program that implements a given agent function? Give an example, or show why one is not possible.
*b.* Are there agent functions that cannot be implemented by any agent program?
*c.* Given a fixed machine architecture, does each agent program implement exactly one agent function?
*d.* Given an architecture with n bits of storage, how many different possible agent programs are there?
*e.* Suppose we keep the agent program fixed but speed up the machine by a factor of two. Does that change the agent function?

**A:**

### 2.7 
**Q:** 
Write pseudocode agent programs for the goal-based and utility-based agents. The following exercises all concern the implementation of environments and agents for the vacuum-cleaner world.

**A:**

### 2.8 
**Q:** 
Implement a performance-measuring environment simulator for the vacuum-cleaner world depicted in Figure 2.2 and specified on page 38. Your implementation should be modular so that the sensors, actuators, and environment characteristics (size, shape, dirt placement, etc.) can be changed easily. (Note: for some choices of programming language and operating system there are already implementations in the online code repository.)

**A:**

### 2.9 
**Q:** 
Implement a simple reflex agent for the vacuum environment in Exercise 2.8. Run the environment with this agent for all possible initial dirt configurations and agent locations. Record the performance score for each configuration and the overall average score.

**A:**

### 2.10 
**Q:** 
Consider a modified version of the vacuum environment in Exercise 2.8, in which the agent is penalized one point for each movement.
*a.* Can a simple reflex agent be perfectly rational for this environment? Explain.
*b.* What about a reflex agent with state? Design such an agent.
*c.* How do your answers to a and b change if the agent’s percepts give it the clean/dirty status of every square in the environment?

**A:**

### 2.11 
**Q:** 
Consider a modified version of the vacuum environment in Exercise 2.8, in which the geography of the environment—its extent, boundaries, and obstacles—is unknown, as is the initial dirt configuration. (The agent can go Up and Down as well as Left and Right.)
*a.* Can a simple reflex agent be perfectly rational for this environment? Explain.
*b.* Can a simple reflex agent with a randomized agent function outperform a simple reflex agent? Design such an agent and measure its performance on several environments.
*c.* Can you design an environment in which your randomized agent will perform poorly? Show your results.
*d.* Can a reflex agent with state outperform a simple reflex agent? Design such an agent and measure its performance on several environments. Can you design a rational agent of this type?

**A:**

### 2.12 
**Q:** 
Repeat Exercise 2.11 for the case in which the location sensor is replaced with a “bump” sensor that detects the agent’s attempts to move into an obstacle or to cross the boundaries of the environment. Suppose the bump sensor stops working; how should the agent behave?

**A:**

### 2.13 
**Q:** 
The vacuum environments in the preceding exercises have all been deterministic. Discuss possible agent programs for each of the following stochastic versions: 
*a.* Murphy’s law: twenty-five percent of the time, the Suck action fails to clean the floor if it is dirty and deposits dirt onto the floor if the floor is clean. How is your agent program affected if the dirt sensor gives the wrong answer 10% of the time?
*b.* Small children: At each time step, each clean square has a 10% chance of becoming dirty. Can you come up with a rational agent design for this case?

**A:**
### 4 Approaches to AI

By distinguishing between human and rational behavior, we are not suggesting that humans are necessarily “irrational” in the sense of “emotionally unstable” or “insane.” One merely need note that ***we are not perfect***: not all chess players are grandmasters; there will be some systematic errors in human reasoning (Kahneman et al.)
#### Thinking Humanly
- The automation of activities that we associate with human thinking, like decision making, problem solving, learning.
- Understand that thinking humanly, doesn't mean reaching the right solution, it simply means thinking like a human. 

#### Acting Humanly
- The study of how to make computers do things at which, at the moment, people are better at doing, functions that require intelligence when performed by people.
-  Similar principal to the Turing test, people consider it to be AI if a machine can act like a human.
- Disagreed upon sometimes because this does not mean that the AI understands what it's doing.
#### Thinking Rationally
- The study of the computations that make it possible to perceive, reason and act.
- The study of this approach, initiated the field called logic. 
- It is said that if you are able to describe a problem in logical notation, you can solve it (not realistic in real life because it is hard to represent informal knowledge in formal terms (i.e when you are not sure something is 100% true), also because the number of facts can't be too large.) 
#### Acting Rationally
- The study of computations and rational agents which acts so as to achieve the best outcome or the best expected outcome. 
- making correct inferences isn’t the only way to act rationally. Sometimes, there’s no definitive right action, but the AI still needs to make a decision.



### Dartmouth Summer Research Project
- The Dartmouth Summer Research Project, 1956 is considered to be the birthplace of AI ***as a field***
- Main goal was to explore how machines use languages, form abstractions and concepts, solve problems now reserved for humans and improve themselves.
- It was planned for 2 months in the summer and was attended by 10 participants.
- Did not achieve their goals, still marked the beginning of AI as a field.

### Turing Test
- Proposed by Alan Turing in 1950, to answer the question 'Can machines think?' (But is actually a test of can machines behave like humans)
- Procedure involves a human evaluator who the machine tries to trick into thinking that the evaluator is communicate with a human.
-  It’s not about how the machine processes information, but whether the machine’s output is indistinguishable from that of a human.

### Chinese Room Thought Experiment
- The argument holds that a digital computer executing a program cannot have a “mind”, “understanding”, or “consciousness”, regardless of how intelligently or human-like the program may make the computer behave
- Searle imagines himself in a room where he receives input in the form of Chinese characters from a slot in the door. Searle, who does not understand Chinese, is given a set of rules in English for manipulating the Chinese characters. The rules instruct him to respond to the input by creating a set of Chinese characters and pushing them out of the room. To those outside the room, it appears as though the room understands and speaks Chinese, but Searle argues that he does not understand Chinese, he is merely manipulating symbols based on a set of rules. This, Searle claims, is what computers do when they process information - they don’t understand the information, they just manipulate it.
### Risks of AI
#### Actual
- Privacy
- Bias
- Legal
- Harm
- Societal (Manipulation of human beliefs/behavior)
#### Hypothetical 
- Superintelligence Singularity
- Consciousness
- Human extinction
#### Challenges
- Regulation
- Ethics


### Intelligent Agents
- An agent is anything that can be viewed as perceiving its environment through **sensors** and acting upon that environment through **actuators**.
- An intelligent agent, is an agent that exhibits intelligent behavior. 
- An agent’s **percept sequence** is the complete history of everything the agent has ever perceived.
- we say that an **agent’s behavior** is described by the **agent function** that maps any given percept sequence to an action, this will be a very large table, infinite,  unless we place a bound on the length of the percept sequence we want to consider. 
- the **agent program** is a concrete implementation, running within some physical system, different from an **agent function**.
#### Rational Agents
- *For each possible percept sequence, a rational agent should select an action that is expected to maximize its performance measure, given the evidence provided by the percept sequence and whatever built-in knowledge the agent has.*


- When an agent is plunked down in an environment, it generates a sequence of actions according to the percepts it receives. This sequence of actions causes the environment to go through a sequence of states. If the sequence is desirable, then the agent has performed well. This notion of desirability is captured by a ***performance measure*** that evaluates any given sequence of environment states.
- It is better to design performance measures according to what one actually wants in the environment, rather than according to how one thinks the agent should behave.
- Consider a vacuum cleaning agent, we might propose to measure performance by the amount of dirt cleaned up in a single eight-hour shift. With a rational agent, of course, what you ask for is what you get. A rational agent can maximize this performance measure by cleaning up the dirt, then dumping it all on the floor, then cleaning it up again, and so on. A more suitable performance measure would reward the agent for having a clean floor. For example, one point could be awarded for each clean square at each time step (perhaps with a penalty for electricity consumed and noise generated) (from the book AI, A Modern Approach).





#### Agent Types
- Be careful when trying to distinguish  **omniscience** and **rationality**, An omniscient agent knows the actual outcome of its actions and can act accordingly (pretty much impossible in reality)
- ***UNIMPORTANT BUT FUNNY*** -  Consider the following example: I am walking along the Champs Elysees one day and I see an old friend across the street. There is no traffic nearby and I’m not otherwise engaged, so, being rational, I start to cross the street. Meanwhile, at 33,000 feet, a cargo door falls off a passing airliner, and before I make it to the other side of the street I am flattened. Was I irrational to cross the street? It is unlikely that my obituary would read “Idiot attempts to cross street.”
- It is important to know that **Rationality is NOT the same as perfection.** Rationality maximizes expected performance, while perfection maximizes actual performance.
- To the extent that an agent relies on the prior knowledge of its designer rather than on its own percepts, we say that the agent lacks ***autonomy***. A rational agent should be autonomous—it should learn what it can to compensate for partial or incorrect prior knowledge.
##### Specifying the task environment (PEAS)
- We group the performance measure, the environment, the agents actuators and sensors under the heading **task environment**, (for the acronymically minded, we call this the **PEAS (Performance, Environment, Actuators, Sensors)**) description
##### Environment Types
- **Fully Observable vs Partially Observable**
	- If an agents sensors give it access to the complete state of the environment at each point in time, we say that the task environment is **fully observable** else it is either **partially observable** or **unobservable**. 
	- If the agent has no sensors at all then the environment is **unobservable**
	- A task environment is effectively **fully observable** if the sensors detect all aspects that are relevant to the choice of action; relevance, in turn, depends on the **performance measure**
- **Single Agent vs Multi Agent**
	- Pretty straightforward, For example, an agent solving a crossword puzzle by itself is clearly in a **single-agent** environment, whereas an agent playing chess is in a **two agent** environment
	- There are subtle issues, for example in a driving agent environment, each of the agents are trying to **maximize** their performance measure, but in this environment maximizing their performance measure means not crashing, reaching in the quickest time, etc , which also does NOT correlate to another agents performance measure,  these environments are called **cooperative multiagent environments** (although a multiagent driving environment is only **partially** cooperative as agents may compete in certain scenarios, trying to get slots in lanes, parking spaces, etc.) 
	- Conversely in chess, a two agent environment, if agent A maximizes their performance measure, it means minimizing agent B's performance measure, these kinds of environments are called  **competitive multiagent environments**. 
	- **Communication** is often seen as rational behavior in multiagent environments, **randomized behavior** is also rational because it avoids the pitfalls of predictability (mostly in a competitive environment).
- **Deterministic vs Stochastic**
	- If the next state of the environment is completely determined by the current state and the action executed by the agent, then the environment is **Deterministic**, otherwise it is **Stochastic**.
	- **Stochastic** generally implies that uncertainty about outcomes is quantified in terms of their probabilities.
	- (In our definition, we ignore uncertainty that arises purely from the actions of other agents in a multiagent environment; thus, a game can be deterministic even though each agent may be unable to predict the actions of the others)
	- We say an environment is **uncertain** if it is not fully observable or not deterministic
	- A **nondeterministic environment** is one in which actions are characterized by their possible outcomes, but no probabilities are attached to them (different from stochastic).
- **Episodic vs Sequential**
	- In an episodic task environment, the agent’s experience is divided into atomic episodes. **In each episode the agent receives a percept and then performs a single action, Crucially, the next episode does not depend on the actions taken in previous episodes**.
	- In sequential environments, on the other hand, the current decision could affect all future decisions.
	- Episodic environments are much simpler than sequential environments because the agent does not need to think ahead.
- **Static vs Dynamic**
	- If the environment can change while an agent is deliberating then we say that the environment is **dynamic** for that agent, otherwise it is **static**.
	- Dynamic environments are continuously asking the agent what it wants to do; if it hasn’t decided yet, that counts as ***deciding to do nothing***.
	- If the environment itself does not change with the passage of time but the agent’s performance score does, then we say the environment is  **semidynamic**.
	- Taxi driving is clearly **dynamic**: the other cars and the taxi itself keep moving while the driving algorithm dithers about what to do next. Chess, when played with a clock, is **semidynamic**. Crossword puzzles are **static**.
- **Discrete vs Continuous**
	- **Discrete Environment**: This type of environment consists of a finite number of distinct states. The changes in the environment, as well as the percepts and actions of the agent operating within it, occur in distinct steps.
	- **Continuous Environment**: In contrast, a continuous environment has an infinite number of possible states that change smoothly over time. The percepts and actions of the agent can also take on a range of continuous values.
- **Known vs Unknown**
	-  **Known Environment**: The agent has complete knowledge about the outcomes of all actions. Full observability is not required.
	- **Unknown Environment**: The agent lacks knowledge about the outcomes of actions and must learn from interactions. Full observability is possible.
##### Agent Types
- **Reflex Agents**
	- The simplest kind of agent is the simple **reflex agent**. These agents select actions on the basis of the current percept, ignoring the rest of the percept history.
	- A **Reflex Agent with State** is an agent that not only responds to its current percept but also maintains an internal state to keep track of the history of percepts. This internal state reflects some of the unobserved aspects of the current state, allowing the agent to handle partial observability.

- **Goal Based Agents**
	- A **goal-based agent** is one that uses knowledge about its current state and the environment, along with a set of desirable situations (goals), to choose actions.
- **Utility Based Agents**
	- A **utility-based agent** aims to maximize a specific utility. The utility can be anything from maximizing profits to minimizing energy consumption. Unlike a **goal-based agent**, a **utility-based agent** doesn’t have a particular goal. Instead, it is designed to find the best solution based on a specific utility. 

- **Learning Agent**
	- A learning agent is an agent that improves its performance over time based on its interaction with the environment

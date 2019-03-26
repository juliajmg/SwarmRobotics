

# CLASSIFICATION FOR COLLECTIVE DECISION MAKING IN ROBOTS SWARMS: The best-of-n-problems. 

- Swarm of robots to make a collective decision over which option, out of n available options, offers the best alternative to satisfy the current needs of the swarm.

- **Options**: domain-specific concepts related to particular scenarios (e.g. foraging patches, aggregation areas, traveling paths). Options are characterized by a **quality** and a **cost**.   
@snapend

@snap[east span-50]
![](TheBestOfNProblems.png)

@snapend

---

### Option quality

@snap[west span-50 text-06]
  - Quality of the option, of primary concern for the objective of the swarm.

  - Robots are programmed to actively measure and estimate their quality and to prefer options whose attributes have certain characteristics.

  - E.g. type, quality or availability of food in a foraging patch.

  - Once evaluated, information of the quality of the option is used to influence the collective decision-making process in favor of the best option.

@snapend

@snap[east span-50 text-06]
### Option cost

- Average time needed by a robot to obtain one sample of the quality of the option.

- Depends on the target scenario, and **robots are not requiered to perform measurements to evaluate it**.

- The cost biases the collective decision-making process indirectly: bias induced by the environment and is not under the control of individual robots.

@snapend 

---

### A) Classification of the best-of-n problem instances:

- Five categories depending on how the option **quality** and **cost** are configured in he application scenario and perceived by the robots.

- Symmetric quality and cost:
**Garnier et al. 2009**, **Francesca et al. 2012**
-  Asymmetric quality and cost: Synergic case
**Garnier et al. 2009** with shelter size.

![](taxonomy_bestNProblems.png)  

---

### Also, quality and cost can be **static** or **dynamic**

  - When static, designers favor collective decision-making strategies that result in consensus decisions.

  - When dynamic, i.e. a function of time, designers favor strategies that result in a large majority of robots in the swarm favoring the same option without converging to consensus.
  - In dynamic, remaining majority of agents that are no aligned with the current collective decision keep exploring other options, and possibly discover new ones, making the swarm adaptive.

- Additionally, a consensus decision corresponding to a large majority rather than unanimity allows swarm systems to swiftly react to perturbations as in the case of fish schools.


---
### B) Classification based on the design


![](DesignBasedClassification.png)

---

### 1. Bottom-up design

**1.1. Opinion-based approaches**

Robots have an explicit internal representation of their favored opinion.

Role of designer is to define the control rules that determine how robots exchange opinions and how they change their own opinion.   

Advantage: generic strategies that can be applied to different application scenarios.

**1.2. Ad-hoc approaches**

Control rules governing interaction between robots were designed to address a specific task.

Strategies not explicitly designed to solve a consensus achivement problem, but the execution results in collective decision.

Studies that focus on problem of **spatial aggregation** and on the problem of navigation of unknown environments.

**Garnier et al. 2009**

---

### 2. Top-down design

Robot controller is derived automatically from a high-level description of the desired swarm behavior.

**2.1. Evolutionary robotics**

Evolutionary computation to obtain a neural network representing the robot controller.

Black-box controllers.

**2.2. Automatic modular design**

Relies on optimization processes to combine behaviors chosen from a predefined set and obtain a robot controller that is represented by a probabilistic finite-state machine.

---

# Self-organization in aggregation papers


## 1.
![](Garnier2009.png)

### Goals

Investigate a self-organized decision-making process from both a mechanic and biological perspective.

Prove cockroaches aggregation behavioral model in robots:
  - The larger the number of staying neighbors, the more likely the animal is to stop and stay beside them.

- Test how collective decision mechanism deals with physically distint oportunities:  
    - How does collective choice scale with group size and changing available space for aggregation?
    - How do differences between the sizes of the two shelters bias collective choice?


**Baseline**: Any constraint that modulates the speed of the self-amplification process at one of the different opportunities can lead that opportunity to win or lose against others.

---

#### Behavioral model

- Modulation of staying time depends on the local perception of proximate neighbors.

Rules:  
- Random walk
- Number or percieved neighbors modulates probability of:
  - Stop inside a shelter
  - Duration of stop
  - Restart motion.


**Hypotesis**

If aggregation is restricted or favored in spatially distinct areas, competition should arise between the potential aggregation sites.


---

#### Experiment

Physical robots:
-  Alice
- 10 individuals

Simulations:  


Settings:
1. Two identical shelters

2. Different radius shelters
  - Big - small
  - Big - medium

![](ExperimentalSetup.png)

---

### RESULTS

![](Identical-shelters.png)

![](Large-medium-shelter.png)

![](Medium-small-shelter.png)

- The collective is able to sense and comapre the size of the shelters during the collectiv decision process.
- Performance not implemented directly in to individual robots.

**A physical property of the environment can also have an influence through the collective dynamics and without any modulation of the individual behavior**

---
### FUTURE WORK

- Larger grups aggregation based on individual density-estimations.

- Counting the number of contacts with other robots encountered while exploring the shelter: the rate of encounters under is likely to grow with the density of robots under this shelter.

- Biological system: ant *Temnothorax albipennis*(Prat 2005).

---

## 3. Self-Organized Aggregations in Swarms of Robots with Informed Robots

### Goals

Study how the introduction of informed robots i.e.(with a preferred aggregation site) impacts the aggregation dynamics.

---

### Experimental conditions

- SIMULATIONS

- Two physically identical shelters, except for their color.

- Informed individuals only stop in preferred shelter (black) and ignore the other (white)

- Proportion of informed robots and group size varied

- Density kept constant

![](conditions_informed.png)

---

### Results

- Symmetry breaking towards preferred shelter of informed individuals.

- Non-linear increase of proportion of robots aggregated in black shelter.
    - The slope gets steeper as proportion of informed individuals increases.


![](PercentageAggregatedRobotsN=100.png)

---

## 3. Using robots to understand social behaviour

### Introduction

#### Spectrum of study

![](scale_study.png)

**Physical robots**  

Fewer assumptions need to be made regarding the environmental properties.  

Laws of physics are included for free in robotic models.

Unexpected outcomes due to inclusion of a physical property that would not have been included in an abstract environment.

#### Understanding of social behaviour  

**Questions adressed**

¿How individuals coordinate their efforts to achieve a common goal?  

- Efficient self-organization processes can occur even with little sensory information.

- Division of labor can take place simply due to differences in local perception, in the absence of inter-individual differences and individual recognition.

- Self-organization can even happen withouth any communication or memory.

¿How social behavior evolves?

¿How communicative behaviour evolves?

---

#### Evaluating robotic models

- Biology does not integrate robotic models.

¿Why?

1. Many robotic studies do not use a **hypothesis driven** approach.

In biology, work consists of experiments designed to test a specific hypothesis.

Robot models have been mostly **exploratory**: explore if inclusions of physical properties will reveal novel aspects of the collective behaviour in question.

Risk of not answering a particular question.

In **hypothesis driven** experiments, controlled manipulations make it easier to understand causal mechanisms, and thus to link the model results to natural phenomena.

---

### Future directions

- Role of individual and kin recognition in collective decision-making.

- Interplay between mechanistic properties that are highly dependent on physical factors, and effects arising over evolutionary time:
    - How social interactions can affect the evolutionary pathways of organisms and the evolution of complex social systems.


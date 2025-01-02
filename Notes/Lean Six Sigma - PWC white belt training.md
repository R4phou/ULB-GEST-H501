#Lean-Six-Sigma = #6-sigma with less statistics.
### Lean
The concept lean = improving efficiency, reducing waste

8 types of wastes: #TIMWOODS
- **Transportation**: Moving items/information
- **Inventory**: Items/information that customer has not received
- **Motion**: Excessive movements within workplace
- **Waiting**: Waiting for information/items to arrive
- **Over processing**: Doing more work than necessary
- **Over production**: Doing work before its needed
- **Defects**: Mistakes and errors that need to be reworked
- **Skills**: Failing to use skills and capabilities of the workforce

Value added activities can be a small percentage of the total and be scattered throughout the process:
- Focus on the waste to lower it

There are 5 main principles:
1. *Identify value* from a customer's perspective
2. *Map value stream*
3. *Create flow* based on "map value stream" to design it such that it is efficient
4. *Establish Pull*, listen to your customer and then produce
5. *Seek perfection*, when it is improved, continue to search for improvement on all the different levels

### Six Sigma
#6-sigma 
- Highly structured method to fine-tune processes
- #todo 

It is really important to **look at the** **variations** and **not the averages**. Because customers feel the effect of variation and not average (example of average depth and you can still drown).

If it is not helping the customer's needs, it is because the output of the process has **too much variation**.

#6-sigma focuses on #quality and the different costs can come from:
- **Poor quality**: *internal* (waste/rework etc) or *external* (complaints/handling compensation for damages/penalties)
- **Good quality**: *appraisal* or *prevention*

#6-sigma is a **goal**, to reach 3.4 #DPMO (Defects Per Million Opportunities). This goal is really high and mostly used in Pharma/Hospitals where mistakes CANNOT happen (life/death situations).
- Often it is a smaller sigma that is used (**4 sigma** is often use (6210 #DPMO)).

### Lean Six Sigma
The goal of combining the two is to address time and defect issues.
- Used in **manufacturing**
- Focus on **improving** the process *to get better results*
- Supported by **methods and tools**
- Focus on **customer needs** to define objectives
- Use **data** to verify progress
- Requires **leadership focus and involvement**
- Requires **change leadership skills**

#Lean:
- The metric is **Time**
- Culture: Empowerment
- Underlying science: Industrial engineering

#6-sigma:
- Metric: **Defects**
- Culture: Top Down
- Underlying science: Statistics

$\implies$ The result is smooth and 

## DMAIC
#DMAIC:
- #Define the project
- #Measure baseline the As-Is process
- #Analyze Identify significant process **factors** (the *x's*)
- #Improve Validate solutions
- #Control: sustain improvement

The belts:
- #white-belt: basic knowledge of what is six-sigma
- #yellow-belt: 2 day formation, can start applying it
- #green-belt: adds statistical part
- #black-belt: expert that know how to use statistics
- #master-black-belt: exceptional, 1/1000

### Define
Here we want to define our problem.
-  Define & Scope of the problem
-  Determine Project objectives and benefits
-  Create project charter
	- There is a template that contains a lot information about the team, champions, problem statement, customers implemented etc.

We need first to define the #business-gap, the issues that we want to fix with our project.
- Define the *major business issues*: sore points related to company goals/deliverables
- Identify *product/services* that impact the business issues
- Identify the *critical product/service features* of the business issue: quality, delivery, price/value
- Identify the *process that are involved* creation

We will then translate these business issues into a **process issues**: what are the process steps that we will need to do to improve our product:
- Quality $\to$ Excessive defects
- Delivery $\to$ Excessive process cycle time
- ...

We then need to **select which problems we will solve** because we cannot use all. Methods exists to find those:
- #pareto analysis, #fishbone etc

To document the process: #SIPOC: Supplier, Input, Process, Output and Customer
- Start with the Process
- Then go left for each process to look at inputs/suppliers
- Then go right for Output/Customers
$\to$ Easier that way

We also need to define **metrics and defects**, basically measure the outputs:
- **Primary metric**
	- How you can measure the success of the project and **must be consistent with the problem statement**
	- Reported as a time series graph of: baseline data, target performance and actual/current performance
- **Secondary metrics**: why we are optimizing
	- Measurement of key output features, cycle time, process resource usage that may improve as a result of meeting objectives using the primary metric
	- Primary metric (Cycle time/production unit) $\to$ Consequential metric (labor hours/production unit)
- **Consequential metrics**:
	- Measure possible unintended consequences of process changes, to keep you from passing your problem to another area.
	- Tip: have the doubters on the team help determine which consequential metrics are key
- Financial metric
- Business metric

Then we develop the problem statements:
- Respond to **What, where, when, how much, how do you know**
- First step in solving a problem is to identify and clearly define the problem
- A #problem-statement:
	- Does not include causes of the deficiency
	- Does not include likely actions or solutions
	- Is clear concise and efficient 

### Measure
#Measure:
- Define the #As-Is process
- Validate measurement system for outputs
- Quantify the process performance

The first step is to #map the process:
- Why?
	- To focus the attention on the process in which the problem occurs
	- To provide information to support the problem solving process
	- Get in-depth understanding of the process
	- Show how the work is actually done vs how they think it is done
	- Help bound the scope of the problem
	- jeannémanqué2
- Types of #process-maps:
	- #SIPOC, Macro map, Process flow diagram, Swimlane flowchart, Value Stream map, etc
- How to create it:
	- 10 steps: 
		- Identify the process
		- Define scopes
		- Gather information on the process (interviews, observations, ...)
		- Identify the key activities
		- Sequence of activities
		- Map connections between them
		- Use visual simbols,
		- Review and validate,
		- Finalize documentation (using software: visio, drawio etc)
		- Maintain and update
#### Value Stream Map
#Value-stream-map has for goal to help you identify possible improvement possibilities by *focusing on the big picture*.
- It provides a common understanding of the current state
- Links material flow to information flow

It is a representation of all material data jaipalasuite

There is a stream from suppliers to customer with us (plant/business) in the middle.

There are multiple flows:
- of people
- of products
- of informations
- of parts (data needed)
- of equipment (method of transmitting)
- of raw materials (transactions)
- of engineering (policy and procedures)

#### Simplification opportunities
The **non value adding operations is waste** and thus needs to be deleted.

#hidden-factory are process steps that are not mapped but that are done, these needs to be identified as they add a lot of stress on people and can slow down the 'official process' that doesn't know about everything then.
#### Validate measurement system for outputs
The idea is to verify whether the data we have is correct, are the metrics ok or not?

We also want to add the error that might come with the measurement to the value we have.

#GAGE 
- Resolution: size of the data category when aaaaaaaaaah
- Precision 
- Accuracy

#Repeatability: **same operator,** same gage, same location, same part
#Reproducibility: **different operator**, same gage, same location, same part


Trying to conduct #MSA:
- Setup: select 30 parts of the process: 50% pass, the rest fails
- Execution
- Analysis
- Evaluation: verify whether it is ok or not

**Gage R&R** used to check whether the measurement system is ok or not. How much is the variation from doing the measurement.
### Analyze
Find the potential causes (X's)
- Like a **judge**, decide on the basis
- For that we use the #fishbone diagram

The #fishbone is a cause-effect diagram that is nice. For example:
- The 4P's
- The 6M's (Man, machine, methode, measurements, materials and mother nature)

The #5-whys helps determine the real cause behind an issue. (Example of the memorial).
### Improve
Can be very broad:
- Generate potential solutions:
	- Using root causes, project goals, discoveries during analysis, ideas from other projects, brainstorming, performance targets, *benchmark ideas* or *best practices*.
	- **Brainstorming**: emphasize **quantity** *over quality*, no criticizing, record all ideas, build on ideas to trigger new ideas

#5S - Sort, Set in order, Shine, Standardize, Sustain
- Creating a clean environment/process to make sure that only what is necessary is there
- Clean the workspace (Shine)
- Set standards fore a consistently organized workplace (Standardize)
- Set discipline, train, maintain and review standards (Sustain)

#Poka-Yoke: mistake prevention, proofing and detection to systematically eliminate errors and disturbances.

#SMED Single minute exchange of die.
### Control
- Create control and monitoring plan
- Implement full scale solution
- Finalize transition

The control phase consists in asking a lot of question:
- What can be done to make sure that the defects stay reduced
- What actions can be taken by the team to ensure the improvement is permanent
- What systems can be put in place to help the functional team maintain the gains routinely
- Do I have buy-in from the important players
- With whom do I leave the project
- When does my role in the project end



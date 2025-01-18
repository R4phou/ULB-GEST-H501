#exercise
Objectives to reach when *designing a logistic network*:
- **Capital reduction**: (choosing public warehouses instead of privately owned warehouses, using common carriers instead of privately owned vehicles) usually comes at the expense of higher operating costs.
- **Cost reduction**: (Privately owned warehouses and vehicles, Optimizing the logistics Processes)
- **Improving Service level** may increase revenues, especially in markets with homogeneous low-price products
- But other such as sustainability et

Examples : ![6_Networks&Planning](6_Networks&Planning.pdf#page=24)Until slide 45
# Storage, Warehousing and Inventory management
## Inventory, DCs and Warehouses
**Reasons** to keep **inventory** are to tackle:
- Unexpected changes demand and lead time
- Economies of scale
- Balance supply and demand
- Contingencies
- Manufacturing bottlenecks
- Price changes

### Warehouse and DCs
The #DC and #warehouse have different **roles**
1. Storage of goods
2. Part of production process
3. Returned good centers
4. Consolidation
5. Breakbulk
6. Postponement
7. #Cross-docking 
8. Transshipment
9. Product-fulfilment Center

The **design** of a #warehouse:![](Pasted%20image%2020250110085929.png)

And the **types** of #warehouse:![](Pasted%20image%2020250110085951.png)

The #warehouse have 3 **components**:
1. Equipment
2. People
3. Storage space

There are a lot of **activities/tasks** for #warehouse![](Pasted%20image%2020250110090131.png)
### Inventory Management
6 **Types** of #inventory: 
- Cycle stock
- Safety stock
- Transit inventory or pipeline inventory
- Speculative stock
- Seasonal stock
- Dead stock

**Costs** of #inventory #cost![](Pasted%20image%2020250110090322.png)
## Transportation
#Transportation systems move goods between origins and destinations.

A **transportation** system designs, arranges, sets up, and schedules freight-transportation orders during a given and *limited time period with technical restrictions at the lowest possible cost*.

$\implies$ 1/3 to 2/3 of total logistic costs
$\implies$ 10 to 20% of the product's price

Multiple channels possible:![](Pasted%20image%2020250110090647.png)
# Logistics network design
The basic **components** of a #logitstics-network:
1. Vendors
2. Products
3. Plants
4. Warehouses/DC
5. Transportation services
6. Customers

The **limitations** of #logistics:
1. Spatial restrictions
2. Temporal restrictions
3. Technical constraints
4. Structural constraints
5. Organizational conditions
6. Economical restrictions
7. Safety requirements
8. Competitive conditions
9. Legal restrictions

The #logitstics-network **performance measures**:
- **Qualitative**:
	- Customer satisfaction
	- Flexibility
	- Effective risk management
- **Quantitative**:
	- Cost minimization
	- Sales maximization
	- Profit maximization
	- Customer response time minimization
	- Lead time minimization

$\implies$ Improvement to logistics network $\to$ 5 to 15% of savings in logistics costs

The **models** are **driven by**:
- Customer service levels
- Location decisions (where is the DC)
- Inventory planning
- Transportation management

The outputs of the #logitstics-network-model are:
- The number of #warehouse, their location, ownership (private/public) and their size
- Allocation of customer demand to supply points (warehouses or plants), allocation to single or multiple supply points. $\to$ How to link the different DCs
- Amount of inventory to be maintained at various locations
- Type of transportation services to use
- Level of customer services to be provided (that can be provided)

Classification of logistic oriented **location problems**:![](Pasted%20image%2020250110091101.png)

When designing we **need to define** the #facility **role** (warehouse, DC, Cross-docking etc), its **location**. Then we need to define the **capacity location**. Finally, **market and supply allocation**, decide how to receive the products and supply at the facilities from the customer.

Obviously, there are some trade-offs between for #logitstics-network-model
- Inventories
- Transportation
- Facilities and handling
- Information

**Variation of** #logistics #cost and #response-time with **number of facilities**:![](Pasted%20image%2020250110091448.png)

The different #types of #logitstics-network: ![6_Networks&Planning](6_Networks&Planning.pdf#page=76)Listed here:
- **Manufacturer storage with direct shipping** 
- **Manufacturer storage with direct shipping and in-transit merge
- Distributor storage with carrier delivery 
- Distributor storage with last-mile delivery 
- Manufacturer/distributor storage with customer pickup 
- Retail storage with customer pickup

SUMMARY - comparative performance of #logitstics-network-model![](Pasted%20image%2020250110092539.png)
### Framework for Network design decisions
![](Pasted%20image%2020250110092837.png)
## Models for Facility and Capacity location
- Maximize the overall profitability
- Many trade-offs during network design
- Network design models used:
	- To decide on location and capacities
	- To assign current demand to facilities and identify Transportation Lanes
![](Pasted%20image%2020250110093311.png)
### Capacitated Facility Location Model
Mathematical model with objective function:
$$Min \sum_{i=1}^{n}f_{i}y_{i}+\sum_{i=1}^{n} \sum_{j=1}^{m}c_{ij}x_{ij}$$
- $n$ the number of potential plant locations/capacity
- $m$ the number of markets or demand points
- $D_{j}$ annual demand from market $j$
- $K_{i}$ potential capacity of plant $i$
- $f_{i}$ the annualized fixed cost of keeping plant $i$ open
- $c_{ij}$ the cost of producing and shipping one unit from plant $i$ to market $j$ (includes production, inventory, transportation and tariffs)

The **outputs**: #decision-variables
- $y_{i}=1$ if plant is open, $0$ otherwise
- $x_{ij}$ is the quantity shipped from plant $i$ to market $j$

The **constraints** are:
- Satisfying the demand: $$\sum_{i=1}^{n}x_{ij}=D_{j}$$ for $j=1,\dots,m$
- Supply cannot be more than capacity$$\sum_{j=1}^{m}x_{ij} \leq K_{i} y_{i}$$for $i=1,\dots,n$
	- Multiply by $y$ to make sure that if the plant is not open then there should not be products to be sent there
- $y_{i}\in \{ 0,1 \}$
#Excel  Exercise 1
### Gravity Location models
![](Pasted%20image%2020250110093748.png)
### Allocating Demand to Production Facilities
$$Min \sum_{i=1}^{n}\sum_{j=1}^{m}c_{ij} x_{ij}$$
under constraints:
- $\sum_{i=1}^{n}x_{ij}=D_j$ for $j=1,\dots,m$, all demand is satisfied
- $\sum_{j=1}^{m}x_{ij}\leq K_i$ for $i=1,\dots,n$, production <= capacity
### The capacitated plant location model with single sourcing
Here the market is supplied by only one factory. So we need to modify the decision variables.

The **outputs**:
- $y_{i}=1$ if factory is located at site $i$, $0$ otherwise
- $x_{ij}=1$ if market $j$ is supplied by factory $i$, $0$ otherwise

The objective function:$$Min \sum_{i=1}^{n}{f_{i}y_{i}}+\sum_{i}\sum_{j}D_{j}c_{ij}x_{ij}$$with constraints:
- $\sum_{i=1}^{n}x_{ij}=1$ for all $j=1,\dots,m$, single sourcing
- $\sum_{j=1}^{m}D_{j}x_{ij}\leq K_{i}y_{i}$ for all $i=1,\dots,n$
- $x_{ij},y_{i}\in \{ 0,1 \}$

## Example and exercises
![6_Networks&Planning](6_Networks&Planning.pdf#page=107)
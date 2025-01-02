#exercise
Objectives to reach when *designing a logistic network*:
- Capital reduction
- Cost reduction
- #todo 
- But other such as sustainability et


# Storage, Warehousing and Inventory management
We keep inventory to tackle:
- Unexpected changes demand and lead time
- Economies of scale
- Balance supply and demand
- Contingencies
- Manufacturing bottlenecks
- Price changes


The #DC and #warehouse have different roles
1. Storage of goods
2. Part of production process
3. Returned good centers
4. Consolidation
5. Breakbulk
6. Postponement
7. #Cross-docking 
8. Transshipment
9. Product-fulfilment Center

The basic components of a logistics network:
1. Vendors
2. Products
3. Plants
4. Warehouses/DC
5. Transportation services
6. Customers

The limitations of logistics:
1. Spatial restrictions
2. Temporal restrictions
3. Technical constraints
4. Structural constraints
5. Organizational conditions
6. Economical restrictions
7. Safety requirements
8. Competitive conditions
9. Legal restrictions

The models are driven by:
- Customer service levels
- Location decisions (where is the DC)
- Transportation management
- Et un 4eme #todo 

The outputs of the #logitstics-network-model are:
- The number of #warehouse, their location, ownership (private/public) and their size
- Allocation of customer demand to supply points (warehouses or plants), allocation to single or multiple supply points. $\to$ How to link the different DCs
- Amount of inventory to be maintained at various locations
- Type of transportation services to use
- Level of customer services to be provided (that can be provided)

When designing we need to define the #facility role (warehouse, DC, Cross-docking etc), its location. Then we need to define the capacity location. Finally, market and supply allocation, decide how to receive the products and supply at the facilities from the customer.

Informations important for network design and decisions:

### Capacitated Facility Location Model
Mathematical model with objective function:
$$Min \sum_{i=1}^{n}f_{i}y_{i}+\sum_{i=1}^{n} \sum_{j=1}^{m}c_{ij}x_{ij}$$
- $n$ the number of potential plant locations/capacity
- $m$ the number of markets or demand points
- $D_{j}$ annual demand from market $j$
- $K_{i}$ potential capacity of plant $i$
- $F_{i}$ the annualized fixed cost of keeping plant $i$ open
- $C_{ij}$ the cost of producing and shipping one unit from plant $i$ to market $j$ (includes production, inventory, transportation and tariffs)

The **outputs**: #decision-variables
- $y_{i}=1$ if plant is open, $0$ otherwise
- $x_{ij}$ is the quantity shipped from plant $i$ to market $j$

The constraints are:
- Satisfying the demand: $$\sum_{i=1}^{n}x_{ij}=D_{j}$$ for $j=1,\dots,m$
- Supply cannot be more than capacity$$\sum_{j=1}^{m}x_{ij} \leq K_{i} y_{i}$$for $i=1,\dots,n$
	- Multiply by $y$ to make sure that if the plant is not open then there should not be products to be sent there
- $y_{i}\in \{ 0,1 \}$
#Excel  Exercise 1
### Allocating Demand to Production Facilities
$$Min \sum_{i=1}^{n}\sum_{j=1}^{m}c_{ij} x_{ij}$$
under constraints:
- $\sum_{i=1}^{n}x_{ij}=D$
- 
#todo  
### The capacitated plant location model with single sourcing
Here the market is supplied by only one factory. So we need to modify the decision variables.

The **outputs**:
- $y_{i}=1$ if factory is located at site $i$, $0$ otherwise
- $x_{ij}=1$ if market $j$ is supplied by factory $i$, $0$ otherwise

The objective function:$$Min \sum_{i=1}^{n}{f_{i}y_{i}}+\sum_{i}\sum_{j}D_{j}c_{ij}x_{ij}$$with constraints:
- $\sum_{i=1}^{n}x_{ij}=1$ for all $j=1,\dots,m$
- $\sum_{j=1}^{m}D_{j}x_{ij}\leq K_{i}y_{i}$ for all $i=1,\dots,n$
- $x_{ij},y_{i}\in \{ 0,1 \}$



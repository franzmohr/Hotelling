# Solving Hotelling Models in Wolfram Mathematica
## Description
The file <code>hotelling.nb</code> contains the functions <code>Hotelling</code> which solves some linear Hotelling models. Currently, the function allows for
- multiple initial product positions,
- entrance of a product at an arbitrary position of an arbitrary firm,
- different (constant) marginal costs of each firm,
- different market sizes.

So far, only linear models are considered. The individual demand schedules are restricted to a negative one-by-one relation between price and demand and a negative one-by-one relation between demand and preference distance for each product.

## Usage
The function <code>Hotelling[positions,entrant,MC,market]</code> requires to enter four starting values:
- <code>position</code> specifies the initial product positions. They have to be entered as a list that contains values of the range [0,1], e.g. <code>{0,.6,1}</code>.
- <code>entrant</code> specifies the position of a new product g that is introduced by an already existing producer n. This is entered as a list of the form <code>{g,n}</code>. If <code>entrant</code> is set to zero, the solution will be obtained for the firms specifiey in <code>position</code> only.
- <code>MC</code> is a list of marginal costs for each firm. If all firms are assumed to have the same marginal costs, only a scalar can be entered. The order of the list entries has to follow the order of the <code>position</code> entries. If it is assumed that a firm introduces a new product, this becomes the order of the final product positions.
- <code>market</code> is a scalar giving the market size.

## Examples
<code>Hotelling[{0,.6,1},0,10,100]</code> solves the Hotelling model with initial product positions at 0,.6 and 1, no entrant, homogenous marginal costs of 10 and a market size of 100.

<code>Hotelling[{0,.6,1},{.3,3},{10,25,10,20},2000]</code> solves the Hotelling model with initial product positions at 0,.6 and 1, where firm 3 introduces a new product at position .3. Firms 1 and 2 have both marginal costs of 10, whereas firm 3 has marginal costs of 25 for its new product and 20 for the other product. The market size is 2000.

## Contributors
Franz Mohr

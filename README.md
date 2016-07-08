# Solving Linear Hotelling Models in Wolfram Mathematica
## Description
The file <code>notebook.nb</code> contains the functions <code>Hotellin</code> which solves some linear Hotelling models. Currently, the function allows for
- multiple initial product positions,
- entrance of a product at an arbitrary position of an arbitrary firm,
- different (constant) marginal costs of each firm,
- different market sizes.

The individual demand schedules are restricted to a negative one-by-one relation between price and demand and a negative one-by-one relation between demand and preference distance for each product.

## Setup
The function <code>Hotelling[positions,entrant,MC,market]</code> requires to enter four starting values:
- <code>position</code> specifies the initial product positions. They have to be entered as a list that contains values of the range [0,1], e.g. <code>{0,.6,1}</code>.
- <code>entrant</code> specifies the position of a new product g that is introduced by an already existing producer n. This is entered as a list of the form <code>{g,n}</code>. If <code>entrant</code> is set to zero, the solution will be obtained for the firms specifiey in <code>position</code> only.
- <code>MC</code> is a list of marginal costs for each firm. If all firms are assumed to have the same marginal costs, only a scalar can be entered. The order of the list entries has to follow the order of the <code>position</code> entries. If it is assumed that a firm introduces a new product, this becomes the order of the final product positions.
- <code>market</code> is a scalar giving the market size.

## Contributors
Franz Mohr

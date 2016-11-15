# Solving Hotelling Models in Wolfram Mathematica
## Description
The file <code>hotelling.nb</code> contains the functions <code>Hotelling</code> which solves some linear Hotelling models. Currently, the function allows for
- multiple initial product positions,
- entrance of a product at an arbitrary position by an arbitrary firm,
- different (constant) marginal costs for each firm,
- different market sizes.

So far, only linear models are considered. The individual demand schedules are restricted to a negative one-by-one relation between price and demand and a negative one-by-one relation between demand and preference distance for each product.

## Usage
The function <code>Hotelling[positions,entrant,MC,market]</code> requires to enter four starting values:
- <code>positions</code> specifies the initial product positions. They have to be entered as a list that contains values from the range [0,1], e.g. <code>{0,.6,1}</code>.
- <code>entrant</code> specifies the position of a new product g that is introduced by an already existing producer n. This is entered as a list of the form <code>{g,n}</code>, where g is in [0,1] and n is the nth place of the firm in <code>positions</code> which is assumed to introduce the product. If <code>entrant</code> is set to the scalar zero, there is no entry and the solution will be obtained for the firms specified in <code>positions</code> only.
- <code>MC</code> is a list of marginal costs for each firm. The order of the list entries has to follow the order of the <code>positions</code> entries. If it is assumed that a firm introduces a new product, the resulting new preference order has to be used. If all firms are assumed to have the same marginal costs, a single scalar can be entered.
- <code>market</code> is a scalar giving the overall market size.

## Examples
<code>Hotelling[{0,.6,1},0,10,100]</code> solves the Hotelling model with initial product positions at 0,.6 and 1, no entrant, homogenous marginal costs of 10 and a market size of 100.

<code>Hotelling[{0,.6,1},0,{10,25,20},2000]</code> solves the Hotelling model with initial product positions at 0,.6 and 1 and no entry. Firms 1, 2 and 3 have marginal costs of 10, 25 and 20, respectively. The market size is 2000.

<code>Hotelling[{0,.6,1},{.3,3},{10,25,10,20},2000]</code> solves the Hotelling model with initial product positions at 0,.6 and 1, where firm 3 introduces a new product at position .3. Firms 1 and 2 have both marginal costs of 10, whereas firm 3 has marginal costs of 25 for its new product and 20 for the other product. The market size is 2000.

## Contributors
Franz Mohr

## Copyright
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

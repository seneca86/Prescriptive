---
title: "Wellyntoy Products"
author: "Prescriptive Analytics"
date: "2024"
---

# Wellyntoy case

## Summary

### Business context

* Dynatron is originally a comic strip and then became a cartoon series

* Wellyntoy decided to produce a character toy based on Dynatron

* Injection moulded toy with moving parts that can become a racing car with few manipulations

* Two Dynatron types: standard and super
Different in size and finish

* Wellyntoy plans for 2010 learning from 2009

### Numbers from 2009:

* Tooling capacity: 150,000 units (£50,000)
* Order quantity: 33,000 standard and 19,000 super
* Sales: 35,000 units (60% standard and 40% super)
* Inventory leftover: 12,000 standard and 5,000 super (due to production delays)

![Model in Open Solver](pictures/background_2009.png)

### Situation for 2010:

* Demand: 150,000 units (min=50,000 units, max=300,000 units)
* Proportion of supers: 40% (min=30%, max=60%)

![Model in Open Solver](pictures/background_2009.png)

* Price for 2010: £4.30 standards, and £5.50 supers

* Cost estimates for 2010
* Capacity costs:
Tooling capacity from 2009 (150,000) is in good shape
£15,000 to increase tooling capacity anywhere between 150,000 and 200,000
£55,000+£15,000 to have capacity over 200,000
* Direct costs: £2.50 for standard and £3.20 for super.
* Selling, royalties, discounts: 9% of gross margin
* Advertising and promotion: 3% of gross margin
* Holding cost: 2% per month based on direct costs
Any excess stock is carried for an average of 6 months

![Model in Open Solver](pictures/setup.png)

### Questions to solve

* Who are the main characters?
  * Danny Keepstone, Marketing Manager
  * Saul Gassman, Product Manager

* What is the main question?
  * How many Dynatron to produce for Autumn 2010? 

* Three different production alternatives

  * Produce 130,000 standards and 95,000 supers (field sales representatives)
  * Produce 80,000 standards and 70,000 supers (production manager)
  * Produce 115,000 standards and 85,000 supers (Gassman, product manager)

* When must be the decision made?
  * By the end of March 2010 (6 months before)

### Profit and loss

$\text{Net Profit} = \text{Gross Margin} - \text{Additional Expenses} - \text{Inventory Carrying Costs} - \text{Capacity Costs}$

$\text{Gross Margin} = (\text{Price}_{st} - \text{Direct Cost}_{st}) \times \text{Sales}_{st} + (\text{Price}_{sup} - \text{Direct Cost}_{sup}) \times \text{Sales}_{sup}$

$\text{Additional Expenses} = 12\% \times \text{Gross Margin}$

$12\% = 9\% \text{ (royalties, etc)} + 3\% \text{ (advertising, etc.)}$

$\text{Sales}_{st} = \min(\text{Demand}_{st}, \text{Avail. Inventory}_{st})$

$\text{Avail. Inventory}_{st} = \text{Leftover09}_{st} + \text{Production}_{st}$

$
\text{Inventory Carrying Costs} = 2\% \times £2.5 \times \text{Leftover}_{10_{st}} \times 6 + 2\% \times £3.20 \times \text{Leftover}_{10_{sup}} \times 6
$

| Total Production                       | Capacity Costs (£) |
|----------------------------------------|-------------------|
| $≤ 150,000$                              | 0                 |
| $150,000 < Total Production ≤ 200,000$   | 15,000            |
| $> 200,000$                              | 70,000            |

## Building up the models

### Sensitivity to one variable

![Model setup](pictures/model_setup.png)

![Best model](pictures/best_model.png)

![Worst model](pictures/worst_model.png)

We can assess the impact of different demand scenarios while keep the optimization as per the base case.

| % of Supers | Net Profit    |
|-------------|---------------|
| 30%         | £227,880      |
| 35%         | £245,940      |
| 40%         | £264,000      |
| 45%         | £249,870      |
| 50%         | £235,740      |
| 55%         | £221,610      |
| 60%         | £207,480      |

| Demand  | Net Profit    |
|---------|---------------|
| 50,000  | £54,640       |
| 75,000  | £106,980      |
| 100,000 | £159,320      |
| 125,000 | £211,660      |
| 150,000 | £264,000      |
| 175,000 | £264,000      |
| 200,000 | £264,000      |
| 225,000 | £264,000      |
| 250,000 | £264,000      |
| 275,000 | £264,000      |
| 300,000 | £264,000      |

![Model setup](pictures/demand_vs_profit.png)


### Sensitivity to two variables

We can explore what would happen if the share of "super" and the total demand changed in an orthogonal way. For that, we will build an Excel data table:


![Data table](pictures/data_table.png)

![Contour plot setup](pictures/contour.png)
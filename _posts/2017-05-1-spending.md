---
layout: page
title: Spending audit, 2016
---

### Methodology
[Mint](http://www.mint.com/) tracks all of my spending. Mint automatically
categorizes transactions into categories like "Pharmacy" or "Rental Car & Taxi",
and I periodically check and change Mint's categorizations.

I exported the data from Mint and, using Pandas, assigned each transaction
to categories that were less granular and more relevant than Mint's categories,
like "transportation" or "work expenses".

Then I classified transactions into an even coarser set of categories,
classifying transactions by their purpose, like "food,", "entertainment",
or "charity."
But many transactions serve multiple purposes. For example,
a $12 restaurant meal provides maybe $3 of food and
$9 of enjoyment. An MBTA pass can get me to work and then to a party.

So I assigned some of the granular categories to multiple
coarse categories. For example, I buy lunch at Harvard partially
because I need to eat and partially so I can spend more time
working instead of cooking, so I assigned ``work food" 50% to "food"
and 50% to "work expenses." I assigned restaurant spending 25% to "food" and
75% to "amusement." However, it was impossible to assign a purpose to many
transactions. Spending on transportation serves many purposes, so I just left it
as "transportation". Cash could have been used for anything, so I lumped it in
with "unknown." 

### Context
I live with my husband in a one-bedroom apartment in Cambridge, MA. I'm a Harvard grad
student. I earned money by teaching at Harvard in the spring, from Harvard
for no reason in the summer, and from working part-time at a data science
start up since the summer. [1]

I got married this year. The wedding cost less than $1000 [2], but people gave
us money, and we actually came out ahead.

I bought an expensive laptop this year, which was by far the largest expense
after food and rent. I also bought a lot of clothing, since I'm at a point in
my life where I shouldn't be wearing shirts from high school and ripped-up
athletic shoes to work. I expect to spend less on clothing in the future.
I spend a lot on convenience; since I'm paid hourly, it's a better financial
deal for me to buy an $8 lunch than to cook it, pack it, and clean dishes
myself. I think I could save time *and* money by cooking a huge amount of
food once a week and pre-packing lunches, but I can't ever seem to make that work.

I made $46,572.50 this year. Since I'm filing jointly it's hard to say what
*I* paid in taxes, but it's about $6,800, leaving an after-tax income of about
$39,800.

My biggest expense after rent is usually charity, and I usually donate at the end of the year.
I took the Giving What We Can Pledge several years ago: I've pledged to donate everything
I make over $34,000 post-tax, and at least 10% of my income. ($34,000 in 2012
in 2012 dollars, $35,264 today.) That left me obligated to donate $3,757 in 2016.
I donated my "2016 donation" of $14,400 to GiveWell in the beginning of 2017 rather than at the end of 2016
for tax reasons (and I'll donate again at the end of the year, and call that
my "2017 donation"). I'm not going to count that here, though.

### Spending by category (granular)

| Category                    | Amount   | Number of transactions | Average per transaction |
| --------                    | :----:   | :--------------------: | :---------------------: |
| Rent                        | 10,350   | 12                     |        862.50          |
| Taxes                       | 6,800    |                        | 
|                   groceries |  2691.47 |                   87   |  30.94
|                      laptop |  2350.38 |                    1   |  2,350.38
|                    clothing |   763.23 |                   12   |  63.60
|                 restaurants |   705.56 |                   45   |  15.68
|                   work food |   672.88 |                   78   |  8.63
|                   utilities |   492.40 |                   21   |  23.45
|               work expenses |   470.42 |                    6   |  78.40
|                      sports |   353.06 |                    6   |  58.84
|                        cash |   290.50 |                    7   |  41.50
|              transportation |   232.83 |                   17   |  13.70
|                     unknown |   215.62 |                    6   |  35.94
|                         CVS |   196.15 |                   23   |  8.53
|           other necessities |   188.76 |                    2   |  94.38
|         books and magazines |   170.57 |                   19   |  8.98
| software for education/work |   167.73 |                    4   |  41.93
|                        hair |   165.00 |                    2   |  82.50
|                   amusement |   148.47 |                   15   |  9.90
|        wisdom tooth removal |   141.80 |                    1   |  141.80
|                        gift |   133.88 |                    7   | 19.13
|                  appearance |    84.00 |                    4   | 21
|            home improvement |    50.75 |                    2   | 25.38
|                      coffee |    39.54 |                   11   | 3.59
| charity                     | 35       |                    1   | 35
|                     website |    13.75 |                    2   | 6.88
|                       other |     1.47 |                    4   | 0.37
|                     wedding |  -503.79 |                   15   | -33.59

### Spending by category (coarse)

Coarse Category | Corresponding Granular Categories | Examples
--------------  | --------------------------------- | --------
entertainment | amusement, 75% of restaurants | Google play music, Felipe's
wedding | wedding | venue, food, alcohol, music
self-improving entertainment | books, magazines, sports | The Economist, rock climbing, trail races
appearance | clothing, hair, appearance | 
education/work/professional development | laptop, website, 50% of work food, noise-canceling headphones, Stata
other necessities | coffee shops, other necessities, CVS | soap, instant coffee, phone
charity | charity | none (in 2016)
unknown | unknown, cash, other | ATM withdrawal
food | groceries, 50% of work food, 25% of restaurants | food
medical | wisdom tooth removal |
transportation | transportation | Uber, bicycle repair, train
housing | rent, utitilities, home improvement |
gifts | gifts | birthday presents
taxes | taxes | W2 withholding


Coarse Category | Spending
--------------  | --------
housing                       |  10893.15
taxes                         |   6,800
education/work                |   3338.72
food                          |   3204.30
appearance                    |   1012.23
entertainment                 |    677.64
self-improving entertainment  |    523.63
unknown                       |    507.59
other necessities             |    424.45
transportation                |    232.83
medical                       |    141.80
gifts                         |    133.88
charity                       |  35
wedding                       |   -503.79

This is a total spending of $27,408, or about $20,608 if you don't count
taxes. I usually spend about $18,000 a year, not counting taxes, so this was an 
average year before the new laptop.
I used Betterment to invest the rest, putting as much as possible in
a Roth IRA.

[1] I develop econometric algorithms. It's a lot of fun. Ask me about it.

[2] Pretty good for 38 people if you ask me!


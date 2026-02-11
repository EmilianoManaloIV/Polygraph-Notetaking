---
NoteType: Theory
NoteCreation: 2026-02-10
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Even Odd Observations
* **Odd #:** Use the absolute middle of the given numbers, medians of quartiles will be averaged.
* **Even #:** Utilize average of the middle two numbers, medians of quartiles will be absolute.
* TAKE OUT MEDIAN WHEN FINDING QUARTILES!
___
## The Data Generating Process
* When we take a sample, it tells the distribution of that exact sample **not** the population.
* **DGP:** explains why that variation exists in the population.
	* Social Factors?
	* Environment?
	* Random Chance?
___
## Population Vs DGP
* Often used interchangeably, however, focuses on the process in creating variation. 
* This makes us think of the variables that influences this variation, as the population is the result of DGP over a long time frame.
___
## The Back And Forth Between Data and the DGP
* **DGP: Bottom-Up Reasoning:** Because of the given data we can infer a certain conclusion.
* **DGP: Top-Down:** We have a theory of a certain of conclusion then test against the data we collect; revise as we go.
```R
#How to simulate a dice
dice_outcomes <- c(1,2,3,4,5,6)
#Simulate a single roll of the dice without replacement
sample(dice_outcomes, 1)
#Simulate a single roll of the dice with replacement
resample(dice_outcomes, 1)
```
___
## From DGP to Population To Samples
```R
#you can just sample with a keyword argument to change the property
smaple(dice_outcomes, 1, sample = TRUE)
```
___
## Small Vs Large Samples
* **Sampling Variation:** Occurs when you sample a population and "caps" the amount of observations. 
* **The Rule Of Large Numbers:** The larger the sample, the closer the distribution represents the population.
___
## Weirds DGPs And Their Samples
* Even with weird distributions, the rule of larger numbers still apply.
___
## Laws Of Large Numbers
* As sample increases, greater the accuracy between the sample and the population.
___

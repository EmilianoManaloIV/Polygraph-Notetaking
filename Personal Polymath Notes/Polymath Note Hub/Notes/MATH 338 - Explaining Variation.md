---
NoteType: Theory
NoteCreation: 2026-02-12
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Examining Distributions
* We examined distribution that focuses on one variable which can be categorical or quantitative; **Univariate Summary**
* We are often interested through in the relationship between two variables
---
## Outcomes And Explanatory Variable
* **Explaining Variation:** Focus on why variables are different and often focuses on one variable predicting another variable; are considered related.
* **Outcome Variable:** Variable that we are trying to predict or explain often knowing as the dependent variable, response variable, output variable.
* **Explanatory Variable:** Variable used to explain or predict the outcome variable also know as the independent variable, predictor variable, treatment variable, or factor
$$\text{Outcome Variable} = \text{Explanatory Variable } +\text{ Other Stuff} $$
$$y = f(x)$$
$$\text{Dependent Variable}=f(\text{Independent Variable})$$
___
## Why This Matters?
* Regression, Modeling, Hypothesis Testing, and Statistical Inference
* *Use Variation In One Variable To Explain Variation In Another*
---
## Visualizing Relationship With Scatter Plots
* **Scatter Plots:** Provide a visual way to explain the relationship between two numerical variables.
* X if often the explanatory variable and Y is often the responsive variable.
* **Patterns:**
	* Positive Correlation (Positive Slope)
	* Negative Correlation (Negative Slop)
	* No Relation (Slope Is Zero)
```R
#Create a scatterplot in R
gf_point(y ~ x, data = dataFrame)
```
---
## Research Design
* We often describe a relationship two variables, but it doesn't always have a causation between each other.
* $\text{Correlation} \ne\text{Causation}$
___
## Problems In Causal Claims
* **Directionality Problem:** Does variable A effect variable B and vice-versa?
* **Confounding Problem:** Lurking variables may effect the relationship between A and B, or effect A & B independently.
___
## Observational Vs Experimental
* **Observational:** We just measure variables without manipulating them, these can reveal patterns but doesn't find causation (survey)
* **Experimental:** Manipulate the experimental variable that creates causal claims (random assignments)
---
## Research Designs
* The separation of true vs misleading causalities.
* Best practices for experiments:
	* sample many
	* randomly assign
	* then compare outcome variable
---
## Why Random Assignment Is Needed?
* Balances **confounding** variables.
* **Random Sapling:** helps with generalizing results in a population.
---
## Considering Randomness Is A Possible DGP
* **Randomness:** is a factor in DGP, we must consider this in our outcome variable influence.
---
## What Does The Data Look Like?
* There is guaranteed variation when collecting and assigning groups at random
```R
#Create a jitter plot with a mean
gf_jitter(outcomeVariable~explanatoryVariable, data = someDataFrame, height = someHeight, width = someWidth) %>%
	gf_model(outcomeVariable ~ explanatoryVariable, color = "someColor")
```
* Also known as **random sampling variation**
---
## Using Shuffle To Simulate Randomness
* We can use the shuffle() function to randomly simulate a given category within a data frame.
```R
shuffle(someDataframe$someVariable)
```
---
## Shuffling Can Help Us Understand Real Data
* We need to make many shuffles to conclude a certain pattern to determine of DGP was created by simple random chance (utilizes the **law or large numbers**)
* We then compare if they are similar or different, thus, we can determine if there may be a relationship or not.
---
## Type 1 Error
* There was a relationship being only created by random chance (coincidence).
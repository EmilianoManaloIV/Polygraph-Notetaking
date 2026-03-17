---
NoteType: Theory
NoteCreation: 2026-02-26
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## What Is A Model And Why We Want One?
* A **model** is a simplified representation of something more complex in the real world. Often known as a **function**.
___
## Why Use A Model?
* Real life is too complex and difficult to calculate, a model is better than having none at all; helps calculate a complex situation.
___
## What Is Error?
* **Error** occurs when there is a difference between what the model provides and what the actual real-life data includes.
* A model will **always be not perfect** and thus prone to error every single time.
___
## Big Idea For Statistics
* We want to predict the outcome of a given model we created
$$\text{Outcome} = \text{Some Variable} + \text{Error}$$
___
## What Makes A Model Good?
* A model that minimizes error, which means there is less difference between the model and actual values measured.
___
## Modeling A Distribution With A Single Number
* A **Statistical Model** is a rule or function the defines a whole entire distribution, that can create a prediction.
___
## Choosing The One Number
* It all depends on type:
	* **Quantitative:** Measure of center (Mean or Median)
	* **Categorical:** Use highest frequency (mode)
* Shape of the distribution:
	* **Bell Shape:** We often use the mean
	* **Skewed:** We often use the median, whatever is closer to the center.
	* **Categorical:** Use the highest frequent group
* **Mean:** is effected by large outliers, median's stay consistent.
___
## Model And Error
* We can then conclude that
$$\text{Data} = \text{Model} + \text{Error}$$
* Less spread often have less errors, more errors are found in those with larger spread.
---
## The Median Vs Mean As A Model
* Both models define different ways to describe the center
	* Median(Middle Value)
	* Mean(Average)
---
## When To Use Which?
* Now strong outliers and symmetrical: Mean
* Skewed Distribution: Median
* Categorical Variables: Use The Mode
* We just prefer the mean most of the time though.
---
## Model Idea
$$\text{Data} = \text{Model} + \text{Error}$$
* Add a line for mean or median
```R
#Add a median to your graph
gf_vline(xintercept = median(someVariable), color = "someColor")
#Add a mean to your graph
gf_vline(xintercept = mean(someVariable), color = "someColor")
```
___
## Exploring The Mean
* Not also known as the **average**, its often regarded the balancing point between **residuals (errors)** above and below it.
$$\sum\text{Deviations From Mean} = 0$$
* Median is robust, mean is sensitive.
---
## Venturing Into The World Of Mathematical Notation
* We use mathematical notation to define our calculations, thus, we can use mathematical notation to represent statistical operations.
$$\text{Mean}=\frac{{\sum y_{i}}}{n}$$
$$0 ={\sum Y_{i}-y}$$
$$y_{1}*y_{2}*y_{3}\dots*y_{n}=\prod y_{i}$$

* We can think of mathematical notation as **recipe** (operations that yield a result) and a **concept view** that represents the relationships between numbers.
---
## DATA = MODEL + ERROR Notation
* A sample model is represented by:
$$Y_{i}=b_{0}+e_{i}$$
$$b_{0}= \text{MODEL}$$
$$e_{i}= \text{ERROR}$$
* A population model is represented by:
$$Y_{i}=\beta_{0}+\epsilon$$
___
## General Linear Model (GLM)
* Thus we can use a model to represent a model, such as Y bar is a representation of a mean
$$\bar{Y}=\frac{{\sum Y_{i}}}{n}$$
---
## Statistics VS Parameters
* **Statistics:** Its a calculation, from a sample, an estimator for a parameter.
* **Parameter:** From a population, estimated, and often unknown.
---
## Summarizing Where We Are
* **Sample Model:**
$$\text{Outcome Variable}=\text{Sample Model}+\text{Error}$$
$$Y_{i}=\bar{Y}+e_{i}$$
$$Y_{i}=b_{0}+e_{i}$$
* **Population Model:**
$$\text{Outcome Variable}=\text{Population Model}+\text{Error}$$
---
## R Notation
* We use LaTeX to express mathematical languages
$$Y_{i}=\hat{Y}_{i}+e_{i}$$
$$Y_{i}=b_{0}+e_{i}$$
$$Y_{i}=\beta_{0}+\epsilon_{i}$$
---
## Class Lab
$$b_{0}$$

$$Y_{i}=2.7 +e_{i}$$
$$\beta_{0}=2.7$$
$$Y_{i}=2.7+\epsilon_{i}$$
$$b_{0}=52$$

$$e_{i}$$
$$Y_{i}=52+e_{i}$$

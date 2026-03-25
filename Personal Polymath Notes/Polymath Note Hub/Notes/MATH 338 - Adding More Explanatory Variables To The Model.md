---
NoteType: Theory
NoteCreation: 2026-03-24
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Adding An Explanatory Variable To The Model
* We **statistics** to explain some degree of **variation**; and we want to predict the outcome.
* The **empty model** does not explain variation; works well as a baseline.
* An **explanatory variable** serves to fill this need.
---
## Visualizing Data With A Histogram
```R
empty_model <- lm(someVariable~NULL, data = someDataframe)

gf_histogram(y~., data = someDataframe) %>%
	gf_facet(.~X) %>%
		gf_model(empty_model)
	
```
---
## Visualizing Data With A Jitter Plot
```R
empty_model <- lm(someVariable~NULL, data = someDataframe)

gf_jitter(y~X, data = someData) %>%
	gf_model(empty_model)
```
---
## Key Concepts
* Empty Model = One Parameter
* We **compare means** between groups explains some **variation**.
* The **error** is still **not explained** by this type of model.
---
## Using R To Fit The Group Model
* We can fit a model using the following:
```R
lm(outcomeVariable~exlamitoryVariable, data = someDataframe)
```
* We then can use this model to graph on overlays
```R
gf_jitter(outcomeVariable~explanatoryVariable, data = someDataframe) %>%
	gf_model(someModel)
#Works vice-versa with facited histograms
```
---
## We Then Can Predict And Select Specific Columns
```R
predict(someModel) 
#We can then select certain collumns
select(collumn1, collumn2, ..., collumnN)
```
___
## Interpreting LM Models
```R
lm(someFormula = explanatoryVariable, data = someDataframe)
#Results in:
Intercept (Baseline Mean Of Some Group)
#And
someCategory + or - the baseline mean
```
---
## GLM Model
$$\text{Outcome Variable}=b_{0}+b_{1}\text{Explanatory Variable}+\text{Error}$$
$$Y_{i}=b_{0}+b_{1}X_{i}+e_{i}$$
* $X_{i}$ serves as a dummy variables that encodes which group mean is associated within the formula.
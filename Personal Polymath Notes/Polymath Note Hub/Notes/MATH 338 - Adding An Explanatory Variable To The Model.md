---
NoteType: Theory
NoteCreation: 2026-03-03
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## The Empty Model
* **Empty Mode (null model, mean model):** Often known as the base model that can compare to more complex models later in the class.
* Lacks any **explanatory variables** and follows the form:
*$$\text{Outcome}= \text{Mean} + Error$$
* Essentially indicates as the mean as the outcome variable.
* Since the mean minimizes **sum of squared residuals**; determines that it would be the best prediction under **least squares regression**
$$\text{SSE: Sum Of Squared Errors}=\sum e_{n}^2$$
---
## How Its Added To Histograms
```R
#How to show a model object on another graph
gf_histogram(someVariableY ~ someVariableX, data = someDataFrame) %>%
	gf_model(some_model)
#You can use linear models to show mean
lm(formula = variableY ~ variableX, data = someDataFrame)
#You can assign this to an object
some_model <- lm(formula = variableY ~ variableX, data = someDataFrame)
```
___
## Generating Predictions From An Empty Model
* The **mean** of the sample is **unbiased**, so its equally too high or low **regression**.
* In an empty model we use for predicting what our next entry might be.
* We often save the predicted values onto the dataframe.
```R
#This is what use to add predicitons to a given a dataframe
someDataFrame$someDataAttribute <- predict(some_model)
```
---
## Generating Predicted Data
* We are often interested in the **residual** or error of a model.
$$\text{Residual} = \text{Data} - \text{Mean}$$
$$\text{Data} = \text{Mean} + \text{Error}$$
```R
#How to calculate a residual
someDataFrame$residual = someDataFrame$someActualValue - someDataFrame$someMean 
```
---
## Important Properties Of Residuals
* **Positive Residuals:** Data point is above the mean
* **Negative Residuals:** Below the mean
* **The sum of all residuals:** Will always be 0
* **The Shape Of Residuals:** Will always represent the original data by the values are shifted.
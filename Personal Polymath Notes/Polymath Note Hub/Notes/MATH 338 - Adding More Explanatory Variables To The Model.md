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
---
## Error Leftover From The Group Model
* We used the empty model represented by:
$$\text{Data}=\text{Model Prediction}+\text{Residual}$$
$$e_{i}=Y_{i}-\hat{Y_{i}}$$
* We now use a different model that takes the mean independently of each group, the predication changes, so the residuals also change; thus the model overall may by above/below in general, but above/below in their own group.
---
## Using R To Calculate Residuals
```R
someModel <- lm(y~x,data=someDataframe)
#We can now predict values
someDataframe$attributePredict <- predict(someModel)
#We can also calculate residuals
someDataframe$attributeResid <- resid(someModel)
#Then we can select certain collumns
head(select(attribute1,attrubte2,attributePredict,attributeResid))
```
---
## GLM Notation
$$Y_{i}=b_{0}+b_{i}X_{i}+e_{i}$$
$$Y_{i}=\text{Actual Value}$$
$$b_{0}+b_{1_{i}}X_{i}=\text{Predicted Value}$$
$$e_{i}=\text{Residual}$$
---
## Graphing Residuals From The Model
* We use residual distributions with histograms; you can see there is more overlap between the residuals, residuals removes gender-based variation.
---
## Error Reduced By The Group Model
* We use the following to measure error:
$$\text{Residual}=\text{Data}-\text{Prediction}$$
$$\text{Square Residual}=(Y_{i}-\hat{Y})^2$$
$$\text{SSE}=\sum{{(Y_{i}-\hat{Y})^2}}$$
---
## Comparing Models
* SSE will always be smaller than SSE/SST; due that another attribute often causes variance which is always more accurate.
$$\text{SSE(Empty Model)}=\sum(Y_{i}-\hat{Y})^2$$
$$\text{SSE(Group Model)}=\sum(Y_{i}-\hat{Y})^2$$
* Models are chosen to minimize SSE
$$\text{Empty Model}=b_{0}$$
$$\text{Group Mean}=b_{0},b_{1}$$
---
## Empty Model
* If SSE < SST: The compared model is more accurate
$$\text{SS Total}=\text{SS Model}+\text{SS Error}$$
---
## Using R To Get SS Error
```R
supernova(modelName)
```
* The error will always be equal to or less than the empty model! Thus gauging how it influences variation or not.
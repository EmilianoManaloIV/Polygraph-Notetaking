---
NoteType: Theory
NoteCreation: 2026-03-10
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Quantifying Total Error Around A Model
$$Y_{i}=\hat{Y} + e_{i}$$
$$\text{Observed}=\text{Predicted}+\text{Error}$$
* In a mean model: $\text{Sum Of Residuals = 0}$; means that errors are balanced from above and below.
* We want to quantify error to measure how the model fits against our actual data.
---
## Sum Of Absolute Deviations (SAD)
$$\sum{|{Y_{i}-\hat{Y}}|}$$
* Subtract the mean from each observation, take the absolute value, and then add
```R
#SAD in R
sum(abs(SomeTable$SomeAttribute))
```
---
## Sum Of Squared Deviations
$$\sum(Y_{i}-\hat{Y})^2$$
$$\sum(\text{Observed Value}-\text{Mean})^2$$
* Makes errors exponentially magnitudes larger, thus being a good candidate to measure the amount of error in a given dataset.
```R
#Hw to square a residual
sum(someTable$someResidual^2)
```
---
## The Beauty Of Sum Of Squares
* **Sum Of Squares Minimizes At The Mean**
* Thus since we use an exponential of function, the pattern is that as the mean is further away, it'll be exponentially bigger; mean is the lowest point of the parabola.
---
## The Mean And SS Go Hand-In-Hand
* We have an empty model of:
$$Y_{i}=\bar{Y}+e_{i}$$
* We can calculate the sum of squares using R:
```R
empty_model <- lm(yVariable~Null, data = someTable)
supernova(empty_model)
```
* Which define **ANOVA**, **Regression Modeling**, and **General Linear Modeling**
---
## Variance
* Sum Of Squares have several flaws, it often relies on sample sizes; means that if there is two tables with different data entries but same spread, the some of squares will be different, and spread will be different though they are the same.
* **SS CANNOT:** express the spread, we need to use variance:
$$s^2=\frac{\sum(Y-\bar{Y})^2}{n-1}=\text{Mean Square}$$
* This is a better estimate and corrects sampling bias. $n-1$ will eventually fade as the sample gets larger. $n-1=\text{Degrees Of Freedom}$
* You can use R to get Variance:
```R
var(someTable$someAttribute)
#or
supernova(empty_model)
```
* Note that some of squares is a different unit, often in the format of $\text{unit}^2$
---
## Standard Deviation
* Square root of variance
$$s=\sqrt{s^2}=\sqrt{\frac{{\sum{Y_{i}-\bar{Y}}^2}}{{n-1}}}$$
* Expressed in the original **UNIT**, easier to interpret then just variance; a measure of spread of data.
---
## Visual Meaning Of Standard Deviation
* **Large SD:** Values highly deviate from the mean
* **Small SD:** Values are close to the mean
* Variance and Standard Deviation for population
$$\sigma^2=\frac{{\sum{x_{i}-\bar{x}}^2}}{N}$$

| Measure            | Sample    | Population |
| ------------------ | --------- | ---------- |
| Mean               | $\bar{Y}$ | $\mu$      |
| Variance           | $S^2$     | $\sigma^2$ |
| Standard Deviation | $S$       | $\sigma$   |
___
## R Commands
```R
#Get the average
mean(dataset$variable)
#Standard deviation
sd(data$variable)
sqrt(var(dataset$variable))
favstats(~variable,data=dataset)
#Variance
var(dataset$varialbe)
#Sum of squares
var(dataset$variable)*(n-1)
supernova(model)
```
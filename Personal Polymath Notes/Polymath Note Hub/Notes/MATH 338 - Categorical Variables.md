---
NoteType: Theory
NoteCreation: 2026-02-17
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Categorical Explanatory Variables Hypothesis With Categorical Variables
* We are switching from using **quantitative** variables to **categorical** variables.
* We describe states of a categorical variable as **levels**
___
## How To Tell A Categorical Variable Explains Variation?
* A categorical variable explains variation through:
	* **Group Centers**
	* **Different Distributions**
	* **Predictions Change By Category**
```R
#How to create a jitter plot
gf_jitter( variable_y ~ variable_x, data = some_data_frame, height = some_height, width = some_width)
```
___
## Using Box Plots To Explore Relationships
* You can use box and whisker plots to explore categorial explanatory variables
```R
#Create a boxplot
gf_boxplot(variable_y ~ variable_x, data = some_data_frame) %>%
	gf_jitter()
#stack it to add jitter points
```
___
## Looking For Explained Variation
* We can compare the groups by:
	* **Medians**
	* **IQR**
	* **Overlap Between Boxes**
	* **Clear Box Separation**
	* **Clear Box Similarity**
___
## Faceted Histogram
* Shows the distribution of the outcome variable separately with each **level**
* This show cases there is some variability within each level as well.
```R
#Create a facited histogram
gf_histogram(~ outcome_variable, data = some_data_frame) %>%
	gf_facet_grid(some_categorical_variable ~ .)
```
---
## Between Group Vs Within-Group Variation
* **Between Group Variation:** Difference between group centers
* **Within Group Variation:** Difference within the group itself
___
## When Does A Facet Of Histogram Become Unhelpful
* Should be limited to a certain amount of categories, since R will create a histogram for every single level state.
___
## Categorical Outcomes
* Most of our outcomes where **quantitative** and utilized **scatter plots** and **histograms** to describe the relationship.
* Now we are switching to the **outcome variable** being **categorical**
___
## Bar Graph For Categorical Outcomes
* **Histogram** cannot be applied, **Bar Graphs** are useful in this regard, however we need to add an explanatory variable.
---
## Faceting By Explanatory Variables
* Give us a better understanding between levels with categorical variables
```R
#Facet the bar graph using 
gf_facet_grid()
#Create a facited bar graph
gf_bar(~outcomeVariable, data = someDataFrame)
	gf_facet_grid(.~explanatoryVariable)
```
___
## Why Proportions Matter?
* **Counts** may not always be the same, thus we like to focus on **proportions** to make better predictions with our outcome variable.
```R
#Create a faceted proportion grpah
gf_props(~outcomeVariable. data = someDataFrame)
	gf_facet_grid(.~explanatoryVariable)
```
---
## Contingency Tables
* Its a table used to describe **two categorical variables** it often displays the frequency and proportion of two categorical variables
```R
#How to make contingency table via counts
tally(outcomeVariable~explanatoryVariable, data = someDataFrame)
#How to use proportion contingency table
tally(outcomeVariable~explanatoryVariable, data = someDataFrame, format = "proportion")
```
* Each columns add to 1 and is considered **normalized**
___
## Choosing The Right Visualization 1 Variable
* **Categorical:** Tally, gf_bar
* **Quantitative:** histogram, 
___
## Choosing The Right Visualization 2 Variables
* Cat-Cat
* Qua-Cat
* Cat-Qua
* Qua-Qua
---
## Adding More Explanatory Variables
* **Multivariate Hypothesis:** We can add more than one explanatory variable 
```R
#How to make a multivirate plots
gf_graphType(color = ~explanatoryVariable2, shape = ~explanatoryVariable3, fill = ~explanatoryVariable3, size = someSize)
```
* You can also use faceting to determine changes between various conditions
```R
gf_facet_grid(outcomeVariable ~ explanatoryVariable)
```
___
## Sources Of Variation
* Variation can be either **explained** or **unexplained**, so **total variation** is the combination of these factors.
___
## Unexplained Variation As Random
* There will always be unexplained variation, we view this as **random** and often view them with a **normal** distribution.
---

---
NoteType: Theory
NoteCreation: 2026-02-03
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[Landing Page]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Concept Of Distribution
* **Distribution**: Analysis of what happens when things vary
* **Distribution Shift Attention**: The studying of how this variation occurs, such as how trees shape the forest.
* How does data or an entry, compare to the pattern of multiple data entries and what does it mean?
___
## Histograms
* A visual tool to help you determine patters at a view point, and only works with quantitative data (numeric, not categorical).
```R
#Create a histogram
gf_histogram(~)
```
* **X-Axis**: Range of values for a certain variable
* **Y-Axis**: Can be anything to measure the frequency or distribution of x-axis
```R
#Want to moidify the bin size (caterized range values)
gf_histogram(y ~ x, bins = numberOfCategories)
#Limit the width of a histogram, which means viewer bin
gf_histogram(y ~ x, binwidth = sizeOfBinWidth)
```
___
## Visualizing Data With Histograms
* Sometimes you want to describe the data in a particular way to make it helpful for you; especially data frames.
```R
#How to show the histrogram of a dataframe
gf_histogram(~Variable_name, data = Data_Frame)
#You can also change the fill, color, and thickness of the histogram
gf_histogram(~Variable_name, data = Data_Frame, fill = "", color = "", linewideth = value)
#You can also add labels by
gf_histogram(~Variable_name, data = Data_frame) %>%
	gf_labs(title = "", x = "", y = "")
```
* Always assume **y is the count** and **x is the variable**.
* **Density Histogram**: Shows the relative frequency between each bin, its a proportional calculation.
```R
#Show a density historgram
gf_dhistogram()
```
___
## Shape Of Distributions
* What do certain patterns mean?
	* **Symmetric**
	* **Skewed**
	* **Uniform**
	* **Unimodal**
	* **Bimodal**
* **Measures of spread**: How do the values vary and by how much?
* **Weird Things**: What values don't make sense or stand out?
```R
#How to draw a line to see the pattern
gf_density()
```
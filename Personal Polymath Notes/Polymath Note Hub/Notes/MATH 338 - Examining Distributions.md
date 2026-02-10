---
NoteType: Theory
NoteCreation: 2026-02-03
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Welcome To Statistics]]
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
___
## The Five - Number Summary
* **Min:** Smallest value in the set
* **Max:** Largest value in the set
* **Median:** The value that is exactly between 50% distribution of the set of values.
* WE can then get the five numbers as:
```R
favstats(~variable, data = data_frame)
#Returns min|Q1|median|Q2|max|mean|sd|n-missing
```
___
## Quartiles And The Five - Number Summary
* Median is the exact position where the amount of cases from the left and right are equal
* If there is an even amount of observations, the median is the average of the two values.
___
## Quartiles
* Keep dividing the observations equally until you have more sections known as quartiles, the data must be sorted
* The width of the intervals doesn't matter.
* The quartile system can reveal the **five number summary**:
	* Minimum $Q_{0}$
	* First Quartile $Q_{1}$
	* Second Quartile - Median $Q_{2}$
	* Third Quartile $Q_{3}$
	* Maximum $Q_{4}$
* You can then describe the **center** and **spread**
	* **Range**: Max - Min
* **IQR**: Spread of the middle 50% values, determines if data are skewed or outliers
	* $Q_{3}-Q_{1}$
___
## Outliers
* Outliers can manipulate how data is analyzed, thus at times we have a general rule of thumb
* **IQR Rule Of Thumb:**
	* Data point larger than $Q_{3} +1.5 *IQR$
	* Data point smaller than $Q_{1}-1.5*IQR$
___
## Box Plots And The Five - Number Summary
* Boxplots can describe the distribution of values and can either be vertical or horizontal.
* You can draw boxplots onto a histogram:
```R
gf_boxplot(~variable_name, data = data_frame) %>%
	gf_histogram()
```
* **N-tile** divvies up the data in an even matter and even sorts it
```R
ntile(n)
```
___
## Outliers On A Box Plot
* Plan to filer out unneeded data that face outlier issues utilizing **IQR** and **filter**
___
## Exploring Variation In Categorical (Factor) Variable
* Utilize a bar graph to determine categorical data
```R
#This is for a data frame
gf_bar(~ categorical_variable, data = data_frame)
#This is used for a singular vector
gf_bar(~vector)
```
* An important part of categorical data is the **center** which is the category with the highest amount of entries.
```R
#Tally values
tally()
#Can add proportion keywrod
format = "proportion"
#you can also display margins (totla observations)
margins = TRUE

```
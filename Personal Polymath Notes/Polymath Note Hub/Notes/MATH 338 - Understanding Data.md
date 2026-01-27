---
NoteType: Theory
NoteCreation: 2026-01-27
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Starting With A Bunch Of Numbers
* Statistics is the study of variation with numbers that mean something in the real world
	* **Describe**
	* **Summarize**
	* **Understand Patterns:**
		* from minimum to maximum
		* frequency tables: how much times a value appears.
	```R
	# Combine 2s into a vector
	bunch_of_2s <- c(2,2,2,2,2,2,2,2,2)
	#Create a vector with varaitation of numbers
	bunch_of_123s <- c(2,1,3,3,2,3,1,2,1)
	#Sort the numbers within the vector
	sort(bunch_of_123s)
	#Tally the frequency of numbers that appear; creates frequency table
	tally(bunch_of_123s)
	```
---
## From Numbers To Data
* We need to dictate a process to take certain information either numerically or categorically from the larger population.
	* **Measurement**: some attribute (categorical or numerical)
	* **Sampling**: process of selecting a sample out of the population
* Organize data in a **data frame**
	* **Rows:** Cases
	* **Columns:** Variables
* Each row is an observation for a case
___
## A Data From Example - MindsetMatters
* R provides some easier ways to explore data
```R
#Mindset matters data set
MinsetMatters
#Shows the first six rows of the data frame
head(MindsetMatters)
#Shows an overview of the data
str(MindsetMatters)
#You can access certain varailbes using "$" sign
MinsdetMatters$Age
```
___
## Frequency Tables And Sorting Data Frames
```R
#Make a frequency table on the values associated with a certain varaibles
tally()
#Sorts the whole data frame based on a single variable
arrange(DataSet, Variable)
```
---
## Measurement
* Process of collecting numbers and categories; we need to make sense of:
	* What is being measured?
	* What type of value is it?
	* How is it being measured?
```R
#Shows first six cases of the dataset
head()
#Shows the last six cases of the dataset
tail()
```
___
## Quantitative And Categorical Variables
* **Quantitative Variables**: Meaningful measurable values (inches, mm, age, etc.)
* **Categorical**: A number that represents a trait (gender, location, etc.)
```R
#Convert a variable into a categorical type
factor()
```
---
## Values And Variables
* **Variable**: A certain trait; something that is measured
* **Value:** Result of something being measured to categorized
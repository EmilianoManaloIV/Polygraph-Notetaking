---
NoteType: Annotations
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
	* Describe
	* Summarize
	* Understand Patterns:
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
---
NoteType: Theory
NoteCreation: 2026-01-22
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[MATH 338 - Statistics For Natural Sciences]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****
## Welcome To Statistics
* The study of variation: differences in data.
* Statistics deals with pattern recognition from this variation, and inferring what these patterns can mean.
* One of the important parts of statics is providing a prediction of what is the future trend.
## What Is Understanding?
* Taking and digesting information at a slow and well practiced state.
## Doing Statistics With R
* Utilize R as an open source way to analyze data.
## Programming With R
* Connect
* Run
* Submit
```R
# This is a comment
# Utilie courkata library
```
## Introduction To R Functions
* Name of the function and the arguments as the parameters of the function
```R
#Summation function
sum(4,5)
```
* R is case sensitive
```R
Sum(4,5)
#Is not the same as
sum(4,5)
#Similiar to
"4"!=4
```
* There is several libraries, functions, and other quirks R functions have.
* Spaces are accepted as arguments
```R
sum (2, 4)
```
* How to simulate coin flips
```R
#Flips a coint one time
rflip(1)
#Flips a coin ten times
rflip(10)
```
* How to assign an object into a variable, use assignment operator
```R
#Assigns value
my_number <- 10
#You can also use =
my_other_number = 10
#Displays value
my_number
my_other_number
```
* You create vector objects using c() function
```R
#Create a vector
a <- c(1,2,3)
#Utilize indexes to access vector components, this one accesses three
a[3]
```
* You can store data in objects in many ways
```R
x <- 2
x <- c(2,4)
x <- 3:8
x <- c("a", "b")
x <- c(true, false)
x <- 5 == 3
```
* R can treat numerical values in text is equal to string
```R
"1" == 1
#This is a TRUE statement
```
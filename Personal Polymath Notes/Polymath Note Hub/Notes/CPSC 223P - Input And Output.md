---
NoteType: Theory
NoteCreation: 2026-03-03
NoteTags:
---
**REFLECTION** *What Did You Learn, Understand, Research?*

**CONNECTION** *What Is Directly Related To This?*
[[CPSC 223P - Python Programming Introduction]]
**SYNTHESIS** *What Is Indirectly Related To This? At Least Three Things*

****

## Output Formatting
* You can change the format of output using:
	* Formatted String Literals
* ```python
	  str.format()
	```
	* Manual methods
---
## String Literals
* Add as f that specifies a formatting placeholder methodology
```python
#Using f to fomrat a string literal
f'This value is {someVariableA}, and other value is {someVaribleB}'
#You can format values using string methods
'This is: {someVariableA}'.format(someVar)
#str function is human readable
str()
#repr is used for an interpenter
repr()
```
---
## Formatted String Literals
* You can use literal string formatting
```Python
f'{someVariable:formatChars}'
#Width formating
f'{someVariable:amountOfSpace}'
#You can convert types
f'{someVariable:!a,!s,!r}'
```
![[Screenshot 2026-03-03 171918.png]]
___
## String format() Method
* Curly brackets still hold values, just a little different
```Python
print('{orderValue:formatChars}'.format(value1))
```
---
## Manual String Formatting
* There is a traditional method to edit strings.
---
## Reading And Writing Files
* Open a file so you access and manipulate it
```Python
#Returns a file
open()
#Two arguments you can use
open(filename, mode)
```
* You can open the file in several different modes
	* **r:** read only
	* **w:** write only
	* **r+:** write and read
	* **\r\n:** end of line windows
	* **\n**: end of line in unix
	* **b:** opens up binary
* End of character is handled in-house within the domain of python and works on both unix and windows.
```Python
#Opens and assignes file object
fileObject = open('nameOfFile','r+')
#Close the file
close(f)
#You can make operations that closes automatically once the operation is done
with open('nameOfFile') as fileObject:
	someOperation()
```
* You can read characters in text mode utilizing:
```Python
#In text mode this is the amout of charas
fileObject.read(charSize)
#In binary its the amount of bytes
fileObject.read(byteSzie)
```
* You can read line by line utilizing, blank likes are \n, python uses a moving cursor, each line has a default \n
```Python
fileObject.readline()
#You can read through a file in its entirety using
for line in fileObject:
	print(line)
```
* You can cast lines into a list
```python
#Cast lines into a list of strings
list(fileObject)
```
* You can use the option to write into a file is a string
```Python
fileObject.write(string)
```
* Tells you where the current position relative to the beginning of the tile
```Python
fileObject.tell()
```
* You can move the cursor with the seek operation
```Python
fileObject.seek(offset, whence)
```
---
## JSON Operations
* **Serialize:** Converting data into a json file or other file format
* **Deserialize:** Converting data from a file format into something usable in a program
```Python
#Import JSON pacakage
import json
#Look into what itmay looks like
json.dumps()
#You can then write it
json.dump(x,jsonFileObject)
#You can then load a json into a python data type
x = json.load(jsonFileObject)
```
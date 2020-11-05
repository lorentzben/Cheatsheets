# Illumia Basespace Sequence Hub CLI
### Ben Lorentz

Python is a wildly useful programming language, these are some clips of code that I have found to be helpful. 

# Finding the current directory
```python
import os 
where_am_i = os.getcwd()
```
# Opening a file 
```python
with open ("filename.txt) as file:
	data = file.readlines()
	
	
with open('writeout.txt','w') as output:
	output.write('hello world!')
	
```

# Writing a nested list to file, not as a csv though
written by this [lovely person](https://stackoverflow.com/questions/47126718/writing-nested-lists-into-a-txt-file)
```python
lst = [['a', 2.0], ['b', 3.0], ['c', 4.0]]

filename = 'test.txt'

with open(filename, 'w') as f:
     for sublist in lst:
          line = "{}, {}\n".format(sublist[0], sublist[1])
          f.write(line)

```

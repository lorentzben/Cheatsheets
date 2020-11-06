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
# Calling bash shell commands
## using os.system
```python
import os

os.system("echo hello world")
```

## using subprocess
```python
import subprocess
from subprocess import PIPE

subprocess.run(["ls", "-lah"])

total 15M
drwxr-xr-x  2 bjl34716 sealab 4.0K Nov  5 14:09 .
drwx------ 20 bjl34716 sealab 4.0K Nov  5 13:53 ..
-rw-r--r--  1 bjl34716 sealab  15M Aug 12 09:59 bs
CompletedProcess(args=['ls', '-lah'], returncode=0)


subprocess.run(["ls"], stdout=PIPE, stderr=PIPE)

CompletedProcess(args=['ls'], returncode=0, stdout=b'bs\n', stderr=b'')


temp = subprocess.run(["ls"], stdout=PIPE, stderr=PIPE)
print(temp.stdout)
bs\n
```
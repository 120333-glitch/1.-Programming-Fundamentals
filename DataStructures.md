
# Software Engineering #  
  
## Key notes from learning Modules, Functions, and Data Structures ##
***
1. Decimal system  
- Uses 0-9, each position is a power of 10, and its easy for us to understand.  
- E.g. 964 = (9*10^2) + (6*10^1) + (4*10^0)

2. Binary system  
 - Decimal is easy for us but bad for computers who us switches -> 0 and 1. Only uses 0 and 1, base 2, each bit represents a power of 2.  
 - E.g. 1011 -> (1*2^3) + (0*2^2) + (1*2^1) + (1*2^0) = 11 (base 10)  
 - Binary representes: Numbers/Characters/Image/Sound/Instruction.  

3. Hexadecimal system  
  - Base 16, uses 0-9 then A-F (A = 10, F = 15). Hexadecimal represents 4 binary bits.
  - Split into sections of 4 with each value having 1|2|4|8 over the top, then each section can equal 0-15 and is assigned a hexadecimal number.
  - E.g. Binary: 10101110 -> 1010 1110 -> 1|0|1|0 1|1|1|0 -> 1(1)|0(2)|1(4)|0(8)  1(1)|1(2)|1(4)|0(8) -> 10  15  -> AE (hexadecmial value)  
  - Used in colours, memory address, file formats, and machine level debugging.  

4. Two's complement
 - Use half the numbers for positive and half the numbers for negative, 0-127 is positive, 128-255 is negative.
 - Computers cant do 12-7 so instead they do 12+(-7), going from -7 and moving 12 spaces forward (imagine a circle of values).
 - If the digit at the front (left hand side) of the binary is 0 then its postivie, if it is 1 then its negative.
 - Computers cant multiply, divide, etc... They can only add but with various methods.



***
Modules:  
- Python comes made with a library of modules called the 'Standard Library'. This contains a set of modules which give you access to many useful functions. E.g. print() allows us to display information to the screen. int(), float(), str() and list() allow us to convert between variable types. len(), min(), max(), sum() allows us to find the length, minimum, maximum and sum of a list.
- You will need to install other packages with 'pip', you can easilyy install these packages on your machine by looking up packages with the Python Package Index.
```
import math
```
- You can choose to import an entire module or...
```
from math import cos
```
- You can choose to import a single section. Be careful when you do this, state 'from' first then 'import' -> ALWAYS.
```
from math import cos, sin
```
- You can also import mutiple with a comma to seperate.
- *Math module is very important, always return to it if unsure!*
- Another important module is 'random':
```
import random

random.randrange(end)
random.randrange(start, end)
random.randrange(start, end, step_size)
```
- However remember its end value is up to but no including itself just like 'for i in range'.
- An important tool in the random function is the shuffle tool for lists:
```
students = ['Archie', 'Betty', 'Veronica', 'Jughead', 'Reggie']
random.shuffle(students)
```
- This automatically randomly shuffles the list and reassigns the values back into the list.
- 
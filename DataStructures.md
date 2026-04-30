
# Software Engineering #  
  
## Key notes from learning Modules, Functions, and Data Structures ##
***
1. Decimal System:
- Uses 0-9, each position is a power of 10, and its easy for us to understand.  
- E.g. 964 = (9 * 10^2) + (6 * 10^1) + (4 * 10^0)

2. Binary System:
 - Decimal is easy for us but bad for computers who us switches -> 0 and 1. Only uses 0 and 1, base 2, each bit represents a power of 2.  
 - E.g. 1011 -> (1 * 2^3) + (0 * 2^2) + (1 * 2^1) + (1 * 2^0) = 11 (base 10)  
 - Binary representes: Numbers/Characters/Image/Sound/Instruction.  

3. Hexadecimal System:
  - Base 16, uses 0-9 then A-F (A = 10, F = 15). Hexadecimal represents 4 binary bits.
  - Split into sections of 4 with each value having 1|2|4|8 over the top, then each section can equal 0-15 and is assigned a hexadecimal number.
  - E.g. Binary: 10101110 -> 1010 1110 -> 1|0|1|0 1|1|1|0 -> 1(1)|0(2)|1(4)|0(8)  1(1)|1(2)|1(4)|0(8) -> 10  15  -> AE (hexadecmial value)  
  - Used in colours, memory address, file formats, and machine level debugging.  

4. Two's Complement:
 - Use half the numbers for positive and half the numbers for negative, 0-127 is positive, 128-255 is negative.
 - Computers cant do 12-7 so instead they do 12+(-7), going from -7 and moving 12 spaces forward (imagine a circle of values).
 - If the digit at the front (left hand side) of the binary is 0 then its postivie, if it is 1 then its negative.
 - Computers cant multiply, divide, etc... They can only add but with various methods.

5. Standard Data Types:
 - Python automatically declares data types:
   1. Char/String -> letters, digits, spaces, symbols -> Stored as numbers using the ASCII code.
   2. Boolean -> If statements, loops, comparison -> Data type stored as only 2 values -> true or false -> Essential in decision making + Help control the flow of a program.
   3. Real data -> Stores values that include a decimal point -> Single precision floating point (32 bits, 1 bit is a sign -/+ -> 0/1) -> Real numbers in some cases cannot be stored accurately.
   4. Integer -> Whole numbers both positive and negative -> No decimal point + Exact values (no rounding) -> Limited range depending on memory.
   5. Data and Time -> also stored as a number -> Normally looks at number of seconds from 1 Jan 1970 -> Dates can be formatted in many in many types, E.g. Short date: 29/4/2026 or Long date: Wednesday 29th April 2026.  

6. Data Structures that support data storage:
 - Arrays: A structure that stores multiple values of the same data type, E.g. TestScores = [78, 82, 25]. BUT - python has no arrays, it uses lists, E.g. TestScores = [78 ,"N/A", 25]. Use index numbers to reference the list, E.g. print(TestScores[0] -> '78').
 - Multidimensional lists:
    ```
    grid = [
      [3,2,1]
      [4,5,6]
      [7,8,9]
      ]
    print(grid[1,1])

    => 5
    ```
- Records: A data structure that stores different pieces of related data, each item may be different data types, E.g. Name: "Rory", Age: 16, IsEnrolled = true. -> Record, however in python we use tuple and dictionary, in tuple order is fixed (cannot change -> immutable), E.g. Student1 = ("Rory", 16, true).
- Dictionary: Stores values as key: data pairs. E.g. 
  ```
  person = {
    "name": "Rory",
    "age": 16
    "IsEnrolled": true
  }
  print(person["name])

  => Rory
  ```
  ```
    people = [

      {"name": "Rory",
      "age": 16
      "IsEnrolled": true
    },
      {"name": "Aaron",
      "age": 5
      "IsEnrolled": false
    },
    ]
  
  print(people[1]["name"])

  => Aaron
  ```


7. Data Structures of arrays, tree, records and sequential files:
 - 

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
- Sometimes we need a probability. This can be achieved using random.random() which produces a random float between 0 (inclusive) and 1 (not inclusive). E.g.  
```
import random

r = random.random()
if r < 0.8:
    print('sunny')
else:
    print('rainy')
```
- To force our random numbers to start at the same point in the sequence every time, we can use a seed. We use
```
random.seed(seed)
```
- Where seed is an integer. Here's an example. You'll see that the program will always generate the same results.
```
import random

random.seed(1)
print(random.random())
print(random.random())
print(random.random())
```
- In this code if you dont keep the random.seed(1) the numbers generated will be random each time. Whereas if you keep it, then the number will generate the same (same seed) each time.


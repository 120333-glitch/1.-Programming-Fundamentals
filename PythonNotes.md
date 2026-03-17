
# Python Notes - Software Engineering #  
  
## Key notes from learning to code python ##
***
Code generally works like this:

	1. Process Top/Bottom
	2. Selection
	3. Looping
***
Variables:
- Must start with a letter (a–z, A–Z) or underscore (_)  
- Cannot start with a number  
- Can only contain letters, numbers, and underscores  
- No spaces or special characters (e.g. @, $, %)  
- Case-sensitive (age, Age, AGE are different)  
- Cannot use reserved keywords (e.g. for, if, class, True)  

Types of variables:  
- int → whole numbers (5)  
- float → decimals (3.14)  
- str → text ("hello")  
- bool → True / False  (must be capital)  
|-> 0 = false, 1 = True  
|-> print(int(True)) -> 1  
|-> print(bool(0)) -> False  
|-> print(x > 3) -> prints a boolean answer
- list → ordered collection ([1, 2, 3])  
- tuple → unchangeable list ((1, 2, 3))  
- dict → key–value pairs ({"a": 1})  
- set → unordered unique values ({1, 2, 3})  
  
Displaying 2 different variable together:  
- print(f"Weight: {weight_text}")  
|-> Concatenation, must have the 'f' before the quote in order to join 2 variables to print. this text joins the text "Weight: " with the variable {weight_text}.  
***
- You can import libraries with set codes in them such as 'random' which can generate random numbers, e.g.
```
import random
number = random.randint(1, 100)
print(number)
```
- You can also place these random numbers in list to make random lists, e.g.
```
import random

numberlist = []
n = int(input("How many numbers do you want to generate? "))
l = int(input("How large do you want the numbers? "))
for i in range(0,n):
    rand = random.randint(0, l)
    numberlist.append(rand)
print(numberlist)
```
***
Arrays/Lists:  
```
fruits = ["apple" , "banana" , "cherry", "mango", "kiwi"]  
```
- If you want an empty list than just make: fruits = []
|-> This is an array, variable containing multiple variables.  
|-> They are base 0, meaning the first value is 0, then 1, then 2, etc...  
|-> e.g. fruits = [0] == apple  
|-> I can also set it to: fruits = [i], then, i = 0 and it does that same.  
|-> print(fruits[1:3]) -> this will list all from position 1 to 2  -> it gets up to but doesn't include the 3rd value.  
|-> print(fruits[:3]) -> this will list from position 0 (start) to 3.  -> it gets up to but doesn't include the 3rd value.  
|-> print(fruits[3:]) -> this will list from 3 to the end of the list. -> it includes the 3rd value and goes onward.
|-> print(months[-3]) -> you can also print using negative integers (starting from back to front), except the last item on the list will hold the value of -1, not zero.  
|-> If you try to print a value out of the range it will give you and error.  
-  You can use list.append(item) to add an item to the list, e.g:  
	animals = ['lion', 'caterpillar', 'elephant']  
	animals.append('bee')  
//Then when you print// ['lion', 'caterpillar', 'elephant', 'bee']
- len(list): Find the number of items in a list  
- min(list), max(list): Find the minimum/maximum value in a list of numbers
- sum(list): Calculate the sum of all the values in a list of numbers
- separator.join(list): join all the elements in a list together with a specified separator.  
|-> print(', '.join(todo)) -> just becomes a regular list with no [] brackets and commas as the seperator -> Note that .join() can only be used on lists containing strings.)  
|-> '\n' (a newline character). Makes the spaces between listed items a new line.  
```
text = 'Hello World!'  
print(list(text))  
```
```
['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd', '!']  
```
|-> This seperates the words into its letters:

```
text = 'Red Orange Green Blue'  
print(text.split(' '))
```
|-> This seperates the words into their own listed items:
```
['Red', 'Orange', 'Green', 'Blue']  
```
|-> You can also split with more than a comma, e.g. a comma and a space: print(weekdays.split(', '))  
Example of application -> 'replace' can be used to replace an occurance of text with something else:  
```
secret = input("secret message: ")  
scramble = input("scramble string: ")  
decoded = secret.replace(scramble, "")  
print(decoded)  
```
 - This prints false because the order of the lists matter:
```
list1 = ['red', 'green', 'blue']  
list2 = ['red', 'blue', 'green']  
print(list1 == list2)  
```
- To check if a value is contained within a list we can use 'in' or 'not in' to determine, e.g.
```
passwords = ['open sesame', 'password', '12345']
password = 'invalid'
while password != 'valid':
    guess = input("Enter password: ")
    if guess in passwords:
        password = 'valid'
    else:
        password = 'invalid'
        print("Not a valid password.")
print("Welcome back!")
```

Tuples:  
- A tuple is like a list but with a few differences, it cannot be changed after creation and uses () brackets.
***
Converting Data Types:   
```
	x = '2'  
	y = '7'  
	print(int(x) + int(y))  
```
|-> This converts the data types by adding the brackets and re-specifying.
	print(float( x + y))  
|-> This converts what is printed to a different data type.
***
Defining Functions:
```
def function_1():  
	print("function")
```
|-> This defines a function that when u write 'function_1()' it will run the code defined at the start.
***
Assigning/Checking Data:  
- x = 2 -> this assign the value of '2' to 'x'.
- x == 2 -> checks if it has the same value.
- x =! 2 -> checks if it does not equal to.
- Also:  'x <= 2' or 'x >= 2' or 'x < 2' or 'x > 2'
- YOU ALWAYS PUT <,> BEFORE THE EQUALS SIGN!
***
And/Or Statements:  
- and: both conditions have to be True to evaluate as True  
- or: only one condition has to be True to evaluate as True
***
If/Else/Elif:  
- if is a keyword  
- The condition must evaluate to either True or False  
- The code inside the if statement only executes if the condition is True  
- ':' is placed at the end of the condition  
- The code inside the if statement must be indented. The indentation defines the code block. This allows you to put multiple lines inside the if statement. The indentation can be done using tab or spaces, as long as you're consistent!  
- Don't forget the colon ':' at the end of the if/else/elif statement.  
```
  if condition:  
		code you execute if condition is true  
  else:  
		code you execute if condition is false  
```


***
Formatting Data:  
```
	age = 10  
	print('You are {} years old'.format(age))  
```
|-> You cannot print a string with an integer, so you can use format to print them together and {} where you want it to go, make sure to leave a '.' between the text and format.  
```
	name = 'Alice'  
	age = 10  
	print('Hi {}, you are {} years old'.format(name, age))  
```
|-> You can also do it for multiple varaibles by listing then in format in the order they are printed
	print('1/3 is approximately {:.2f}'.format(1/3))  
|-> The {:.2f} means... ':' → starts the formatting instructions, '.2' → means 2 decimal places, 'f' → means fixed-point (decimal) for. *ALSO MAKE SURE ITS FLOAT VAR*  
```
number = float(input("Enter a number: "))  
print("{}".format(round(number)))  
```
|-> You can use the inbuilt python 'round' function to round to the nearest whole number.  
***
Errors:

|-> NameError: A variable of the specified name cannot be found.
|-> SyntaxError: The structure of the code is invalid.
|-> TypeError: An operation is being applied to variables of the wrong type.
|-> ValueError: A function or operation has received a value of the wrong type.
***
Pseudo-code:  
- Sometimes it can be useful to write algorithms in code form without the syntax of a specific language. We can do this using pseudocode. This is a way of writing code in a format that is easy for a human to read. The exact symbols and keywords may vary depending on the convention you use. 
```
IF condition A THEN  
    process 1  
ELSEIF condition B THEN  
    process 2  
ELSEIF condition C THEN  
    process 3  
ELSE  
    process 4  
ENDIF  
```
<!> make sure to remember the 'ENDIF'

***
Flowcharts:
    
- Flowcharts are used to represent the flow of a program. These diagrams are read from top to bottom and left to right, following the flow of the arrows. There are specific symbols that should be used to indicate specific control structures, as show below:  
- Process - Rectangle: Used for creating or modifying data within a program, e.g. creating variables or performing calculations.
- Input/Output - Parallelogram: Used when the program is reading in information (e.g. input()) from the user, or providing the user with information (e.g. print()).
- Decision - Diamond: Used for conditionals, i.e. if-elif-else statements any time there is a point in the program where we check if something is True or False.

***
Code Testing:  
- Input/outputs pairs that are considered 'failing' are when they don't output the correct/intended message.
- Paths are not singular routes but entire lines (in a flow chart) that it follows to the end. They can diverge to make multiple routes at if/else statements.
- When testing with boundary values you want to make sure to have a range of inputs that follow every route in order to test every possible output.
***
Emojis:  
- You are able to print emojis, as long as you know their unicode. E.g. print("\U0001f600") -> makes a smiley face, and  print("\U0001f641") -> makes a sad face.  
***
Loops:  
- In Python, we can repeat code using loops. There are two types of loops: while loop, for loop  
- while condition: code that executes while condition is true -> IT DOES NOT LEAVE THE LOOP UNTIL THE WHILE STATEMENT IS TRUE!  
```
colours = ['red', 'yellow', 'pink', 'green', 'purple', 'orange', 'blue']  
print(colours[0])
```
- This prints the first (in the 0 place) object from the list.  

```
i = 0  
while i < len(colours):  
	print(colours[i])  
    i = i + 1  
```
- This will go through the entire list and print each colour (remember that all this sentence MUST be in lower case ofr syntax)ntto
- For loops: 
```
for variable in iterable:
```
```
for number in [1, 5, 8, 2]:
    print(number)
```
This code prints:
```
1
5
8
2
```
- Runs through each number in the list until its complete.
- You can also modify values to what you print, e.g.
```
for value in [3, 1, 4, -2, 3]:
    print(value + 1)
```
- You can also loops through letters e,g.
```
for letter in ['A', 'B', 'C']:
    print(letter)
```
- Important note: if you want to print '_/\' you need to write: 
```
print("_/\\")
```
- This is  because \ is considered the break of the statement so you need to add another to counter-act it.
- These are the range functions for a set of numbers you select:
```
range(end)
range(start, end)
range(start, end, step_size)
```
- This code prints from 0-4, but not 5 because it ends beofre then:
```
for i in range(5):
    print(i)
```
- This code runs through a list of values:
```
for i in [0, 1, 2, 3, 4]:
    print(i)
```

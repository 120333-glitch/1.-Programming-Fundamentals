
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
Arrays:  
- fruits = ["apple" , "banana" , "cherry"]  
|-> This is an array, variable containing multiple variables.  
|-> They are base 0, meaning the first value is 0, then 1, then 2, etc...  
|-> e.g. fruits = [0] == apple  
***
Converting Data Types:   

	x = '2'  
	y = '7'  
	print(int(x) + int(y))  
|-> This converts the data types by adding the brackets and re-specifying.
	print(float( x + y))  
|-> This converts what is printed to a different data type.
***
Defining Functions:

def function_1():  
	print("function")
|-> This defines a function that when u write 'function_1()' it will run the code defined at the start.
***
Assigning/Checking Data:  
- x = 2 -> this assign the value of '2' to 'x'.
- x == 2 -> checks if it has the same value.
- x =! 2 -> checks if it does not equal to.
- Also:  'x <= 2' or 'x >= 2' or 'x < 2' or 'x > 2'
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

  if condition:  
		code you execute if condition is true  
  else:  
		code you execute if condition is false  



***
Formatting Data:  
	age = 10  
	print('You are {} years old'.format(age))  
|-> You cannot print a string with an integer, so you can use format to print them together and {} where you want it to go, make sure to leave a '.' between the text and format.  
	name = 'Alice'  
	age = 10  
	print('Hi {}, you are {} years old'.format(name, age))  
|-> You can also do it for multiple varaibles by listing then in format in the order they are printed
	print('1/3 is approximately {:.2f}'.format(1/3))  
|-> The {:.2f} means... ':' → starts the formatting instructions, '.2' → means 2 decimal places, 'f' → means fixed-point (decimal) for. *ALSO MAKE SURE ITS FLOAT VAR*  
number = float(input("Enter a number: "))  
print("{}".format(round(number)))  
|-> You can use the inbuilt python 'round' function to round to the nearest whole number.  
***
Errors:

|-> NameError: A variable of the specified name cannot be found.
|-> SyntaxError: The structure of the code is invalid.
|-> TypeError: An operation is being applied to variables of the wrong type.
|-> ValueError: A function or operation has received a value of the wrong type.
***


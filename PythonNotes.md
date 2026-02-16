Code generally works like this:

	1. Process Top/Bottom
	2. Selection
	3. Looping

Variables:
- Cant start with number, can contain one though
- Cant have a space, must use '_'
- 

Displaying 2 different variable together:
- print(f"Weight: {weight_text}")
|-> Concatenation, must have the 'f' before the quote in order to join 2 variables to print. this text joins the text "Weight: " with the variable {weight_text}.

Arrays:
- fruits = ["apple" , "banana" , "cherry"]
|-> This is an array, variable containing multiple variables.
|-> They are base 0, meaning the first value is 0, then 1, then 2, etc...
|-> e.g. fruits = [0] == apple


Converting Data Types:
	x = '2'
	y = '7'
	print(int(x) + int(y))
|-> This converts the data types by adding the brackets and re-specifying.
	print(float( x + y))
|-> This converts what is printed to a different data type.


Defining Functions:

def function_1():
	print("function")

|-> This defines a function that when u write 'function_1()' it will run the code defined at the start.

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

Errors:

|-> NameError: A variable of the specified name cannot be found.
|-> SyntaxError: The structure of the code is invalid.
|-> TypeError: An operation is being applied to variables of the wrong type.
|-> ValueError: A function or operation has received a value of the wrong type.


# Need to reformat! #
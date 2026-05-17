# OOP - Object Oriented Paradigm #
## Programming Fundamentals ##
***
- Object-Oriented Programming (OOP) is a programming paradigm, which means that it is an approach to writing and structuring programs.
- In OOP we program add the concept of objects. In the programming fundamentals module we focused on procedural programming where we constructed programs using only functions and procedures.
- Example: You can see there are placeholders for the BSB number, account number, balance and holder name attributes. This class also has the methods deposit, withdraw and calculate interest. 
- Instances: An instance is a specific realisation of the class that has actual values assigned to the attributes.
- Abstraction: Classes and objects allow programmers to abstract the implementation details of an object by defining methods.
- Encapsulation: Bundling attributes and behaviours into a single class and individual instances is called encapsulation.
- Classes: A class is the type of an object. The class definition specifies the attributes (properties) and methods (behaviours). Think of a class as a blueprint, from which we will make real objects.
  ```
  class ClassName:

    def __init__(self, parameter_1, ..., parameter_n):
        # Set values here
  ```
- The constructor function is denoted in Python with the name '_ _ init _ _'
- Example of a triangle:
  ```
  class Rectangle:

    def __init__(self, height, width, colour):
        self.height = height
        self.width = width
        self.colour = colour
    ```
- For this class we can create an instant under the name 'red_rect' where we specify the height as 4, width as 2 and colour as red.
  ```
  red_rect = Rectangle(4, 2, "red")
  ```
- Instance attributes are accessed using . between the instance and the attribute name, e.g.
  ```
  class Account:

    def __init__(self, bsb_number, account_number, balance, holder_name):
        self.bsb_number = bsb_number
        self.account_number = account_number
        self.balance = balance
        self.holder_name = holder_name

  batman_account = Account("689716", "62228626", 19.39, "Bruce Wayne")

  print(batman_account.balance)  -> *Just want to print the balance*
  ```
- When we write self.attribute = new_value in the constructor, we are setting the instance attribute. However, we can also assign new overwritten values, (for the code above) e.g.
  ```
  batman_account.balance = 24.89
  ```
- The self parameter of __init__ is a variable that references the current instance that is being created. Recall that a class definition is a blueprint, so self is a way of specifying which instance is being affected by the blueprint.
- A method is a function, which is defined for a class and can only be called on an instance.
- Methods are called by using using . between the instance object and the method name.
  ```
  instance.method(argument_1, ..., argument_n)
  ```
- Inside the class you can can define method which is seen as an action that can be performed by the created object. You can bring external parameters into the action that affect the object, e.g.
  ```
  def __init__(self, name, fuel_capacity):
        self.name = name
        self.fuel_capacity = fuel_capacity
        self.fuel_weight = 0
  def refuel(self, amount):
        self.fuel_weight += amount
  ```
  - In this, there are the set characteristics of the object, then in the refuel method (function) we bring in 'amount' which is/can be inputed by the user to affect the fuel_weight characteristic.
- Attributes: Python also supports class level attributes, which are attributes shared across all instances. This is useful because it would be wasteful for instances to store shared data inside every instance.
  ```
  class ClassName:

    attribute_1 = value_1
    attribute_2 = value_2

    def method1(self, parameter_1, ..., parameter_n):
        # do something
        return # optional
  ```
- Classes can also have associated methods, which are useful for managing class attributes. Class methods are defined by using the @classmethod decorator immediately before the method and by setting the first parameter to cls, which is a reference to the class rather than the instance. -> OR (simple terms) modifies at a class level, modifies the variable of every object made through the class.
  ```
  class ClassName:

    @classmethod
    def class_method1(cls, parameter_1, ..., parameter_n):
        # do something
        return # optional
  ```
- Note! Remember when using a method and calling a vriable from the constructor to always use self.variable_name -> not just variable_name
# OverView:

Object Oriented Programming help us representing things in our code:
* It allow us to represent data as one-to-one relationship to business problems.

## In object oriented programming two big things
* Classes 
* Object

# Class:

A class is a collection of objects. A class contains the blueprints or the prototype from which the objects are being created.It is a logical entity that contains some attributes and methods. 
To understand the need for creating a class let’s consider an example,

* Example 1:
let’s say you wanted to track the number of dogs that may have different attributes like breed, age. If a list is used, the first element could be the 
dog’s breed while the second element could represent its age.

* Example 2:
If we want to write software to work with customer we could create a customer class and then give it to attribute 

# Some points on Python class:  

* Classes are created by keyword class.
* Attributes are the variables that belong to a class.
* Attributes are always public and can be accessed using the dot (.) operator. 
## Eg.: Myclass.Myattribute

```python
class Customer:
    pass
```

# Object:

The object is an entity that has a state and behavior associated with it. It may be any real-world object like a mouse, keyboard, chair, table, pen, etc. Integers, strings, floating-point numbers, even arrays, and dictionaries, are all objects. More specifically, any single integer or any single string is an object.
## Examples:

* The number 12 is an object
* the string “Hello, world” is an object 
* a list is an object that can hold other objects and so on

# An object consists of :

* State: It is represented by the attributes of an object. It also reflects the properties of an object.
* Behavior: It is represented by the methods of an object. It also reflects the response of an object to other objects.
* Identity: It gives a unique name to an object and enables one object to interact with other objects.

```python
c = Customer("Hamna", "Gold")
```

# The self  
Class methods must have an extra first parameter in the method definition. We do not give a value for this parameter when we call the method, Python provides it
If we have a method that takes no arguments, then we still have to have one argument.
This is similar to this pointer in C++ and this reference in Java.
When we call a method of this object as myobject.method(arg1, arg2), this is automatically converted by Python into MyClass.method(myobject, arg1, arg2) – this is all the special self is about.

# The __init__ method 
The __init__ method is similar to constructors in C++ and Java. It is run as soon as an object of a class is instantiated. The method is useful to do 
any initialization you want to do with your object.

## Coding:
```python
class Customer:
    def __init__(self, name, membership_type):
          self.name = name
          self.membership_type = membership_type
          print("Customer created")
c = Customer("Hamna", "Gold")
print(c.name, c.membership_type)
```
# Object Oriented Programming Principles:

There are three principles of OOP:

* Encapsulation
* Inheritance
* Polymorphism

# Encapsulation:

Encapsulation is one of the fundamental concepts in object-oriented programming (OOP). It describes the idea of wrapping data and the methods that work on data within one unit. This puts restrictions on accessing variables and methods directly and can prevent the accidental modification of data. 
To prevent accidental change, an object’s variable can only be changed by an object’s method. Those types of variables are known as private variables.

```python
# Creating a Base class
class Base:
    def __init__(self):
        self.a = "Hamna"
        self.__c = "Hamna"
 
# Creating a derived class
class Derived(Base):
    def __init__(self):
 
        # Calling constructor of
        # Base class
        Base.__init__(self)
        print("Calling private member of base class: ")
        print(self.__c)
 
 
# Driver code
obj1 = Base()
print(obj1.a)
```

# Inheritance:

Inheritance is the capability of one class to derive or inherit the properties from another class. The class that derives properties is called the derived class or child class and the class from which the properties are being derived is called the base class or parent class. The benefits of inheritance are:

* It represents real-world relationships well.
* It provides the reusability of a code. We don’t have to write the same code again and again. Also, it allows us to add more features to a class without modifying it.
* It is transitive in nature, which means that if class B inherits from another class A, then all the subclasses of B would automatically inherit from class A

# Polymorphism:

Polymorphism simply means having many forms. 
## For example, 
we need to determine if the given species of birds fly or not, using polymorphism we can do this using a single function

```python
class Bird:

	def intro(self):
		print("There are many types of birds.")

	def flight(self):
		print("Most of the birds can fly but some cannot.")

class sparrow(Bird):

	def flight(self):
		print("Sparrows can fly.")

class ostrich(Bird):

	def flight(self):
		print("Ostriches cannot fly.")

obj_bird = Bird()
obj_spr = sparrow()
obj_ost = ostrich()

obj_bird.intro()
obj_bird.flight()

obj_spr.intro()
obj_spr.flight()

obj_ost.intro()
obj_ost.flight()
```

In Python, Polymorphism lets us define methods in the child class that have the same name as the methods in the parent class. In inheritance, the child class inherits the methods from the parent class. However,
it is possible to modify a method in a child class that it has inherited from the parent class. This is particularly useful in cases where the method inherited from the parent class doesn’t quite fit the child class. In such cases, we re-implement the method in the child class. This process of re-implementing a method in the child class is known as Method Overriding.

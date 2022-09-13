# Introduction:

When we work on python projects, it’s not a good practice to have all our python code in one single python file (.py).
We are better off splitting our code, classes, functions and variables thoughtfully in separate python files (.py files), aka modules.
Python allows us to import code in one module for use in other modules.

# What is Module and Package?

## Module:
A module is a pythonic statement which contains multiple functions in it. Modules act as a pre-defined library in the code, which is accessible to both coder and user.A Python module is any Python files with a .py extension. It can be imported into python without the .py part.

## Package:
A Python package is nothing but a collection of modules along with a __init__.py file. The modules can also be arranged in hierarchy of folders inside a package.
Just by adding an empty __init__.py file to the in the folder, Python knows it is a Package.

# Example:
The python file games.py can be imported in python as a module. In fact, the type such an imported object is module.

```python
# Import the games.py file as a `games` module
import games
type(games)
```

* Inside the python module (the .py file) we can define one or more class and import them.

```python
# Import a class from the file
from games import Game
```

# Importing module from a package

We can import modules from packages using the dot (.) operator.

* For example, if we want to import the start module it can be done as follows:

```python
import Game.start
```

Now, if this module contains a function named select_difficulty(), we must use the full name to reference it.

```python
Game.start.select_difficulty()
```

# Difference Between Packages and Modules

* A python package works on a library, defining the codes as a single unit of any particular function.
* Modules are a separate library themselves, which have inbuilt functions.


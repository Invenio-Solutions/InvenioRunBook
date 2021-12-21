# Python Best Practices:

>> InvenioLsi continously strives to incorporate the best practices that must be followed during a code design to facilitate an effeicent and sustainable application.

## Naming Styles in Python:

- It is advised that we should follow a similar naming pattern while writing code. PEP-8 is a styling guideline offered by the community that tells us how we should choose and define our naming conventions for our python program.
- We are going to discuss a few of the major naming convention best practices from this guideline below.

    - **Variables**: 
        - variable, short_variable, this_is_a_long_variable
        - Use meaningful words variables that describe the type of data that we are using the variable for. Long variables are advised to be separated using underscores, which helps in enhanced readability.

    - **Classes**
        - Class, LongClassName
        - While writing class names in python, we should use CamelCase. 

    - **Methods**
        - class_method(arg_a, arg_b), this_is_a_long_class_method()
        - A method is defined inside a class to get or set specific attributes of the class. While writing code for methods, the preferred way is to use all lowercase alphabets and separate the words by using underscore. Also, our method might take arguments, for which we can name our arguments in the same way our name of method names, by using underscores as separators between words.

    - **Protected Methods**
        -  _protected_method(self, …)
        - Protected methods are used inside class objects within python. These methods are written with a starting underscore in front of the method name.

    - **Private Methods**
        - __private_method(self, …)
        - Private methods are also used inside class objects within python. These methods are written with a double underscore in front of the method name.

    - **Functions**
        - function(), short_function()
        - We can use the same naming conventions for functions and methods. Both can be separated by using underscores.

    - **Constants**
        - CONSTANT, THIS_IS_A_LONG_CONSTANT
        -  We should use uppercase letters to name a constant and separate those using underscores as well. We can define long or short constant names based on the purpose of the constant that is being used in the context.

    - **Module**
        - module.py, long_module_name.py
        - A module is a python that we can import into our code while writing programs. It is essentially imported as a python object into our code that we can use to refer and bind values to. We should use all lowercase letters for naming our modules and use underscores as separators.

    - **Package**
        - mypackage, shortpackage
        - A package is a collection of one or more python files that together serve a specific purpose. A package can also be a directory that contains a few python modules along with a __init__.py file.

## Python Simple tips:

- **Checking the memory of our python objects** : When we create variables or data frames in python, o It is advised that we efficiently check the memory of our variables while writing our code.

- **Returning multiple values from Functions**: This significantly helps in writing simpler code rather than combining all the variables to a list or dictionary. 

- **Joining strings in python** : Python offers a .join method using which we can concatenate all the strings from a given list.

- **Inline Documentation**: While we program with python, sometimes it becomes essential to document the purpose of our code block. PEP-257 introduced a concept of using docstrings within we python code that helps us documents our methods and classes easily. 


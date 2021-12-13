# Python Best Practices

## Naming Styles in Python:
- When you start programming in python or any other language, a lot of the effort goes into deciding meaningful class names, variables, method names etc. Although it differs from developer to developer, it is often advised that we should follow a similar naming pattern while writing code. PEP-8 is a styling guideline offered by the community that tells us how we should choose and define our naming conventions for our python program.
- We are going to discuss a few of the major naming convention best practices from this guideline below.

    - Variables: 
        - variable, short_variable, this_is_a_long_variable
        - Use meaningful words variables that describe the type of data that you are using the variable for. Long variables are advised to be separated using underscores, which helps in enhanced readability.

    - Classes
        - Class, LongClassName
        - While writing class names in python, you should use upper case alphabets for each of the words. This style of writing words is called CamelCase, popular while writing class names in many other programming languages as well. Do not use hyphens or underscores to separate the words in class names.

    - Methods
        - class_method(arg_a, arg_b), this_is_a_long_class_method()
        - A method is defined inside a class to get or set specific attributes of the class. While writing code for methods, the preferred way is to use all lowercase alphabets and separate the words by using underscore. Also, your method might take arguments, for which you can name your arguments in the same way you name of method names, by using underscores as separators between words.

    - Protected Methods
        -  _protected_method(self, …)
        - Protected methods are used inside class objects within python. These methods are written with a starting underscore in front of the method name.

    - Private Methods
        - __private_method(self, …)
        - Private methods are also used inside class objects within python. These methods are written with a double underscore in front of the method name.

    - Functions
        - function(), short_function()
        - A function is something similar to a method, the only difference is that a function is not associated with a class. You can use the same naming conventions for functions and methods. Both can be separated by using underscores.

    - Constants
        - CONSTANT, THIS_IS_A_LONG_CONSTANT
        - Constants are values in python that have the same value throughout the execution flow and it is assigned once during the initialization. You should use uppercase letters to name a constant and separate those using underscores as well. You can define long or short constant names based on the purpose of the constant that is being used in the context.

    - Module
        - module.py, long_module_name.py
        - A module is a python that you can import into your code while writing programs. It is essentially imported as a python object into your code that you can use to refer and bind values to. You should use all lowercase letters for naming your modules and use underscores as separators.

    - Package
        - mypackage, shortpackage
        - A package is a collection of one or more python files that together serve a specific purpose. A package can also be a directory that contains a few python modules along with a __init__.py file.

## Python Simple tips:
- Check the memory of your python objects: When you create variables or data frames in python, often it becomes challenging if you are allocating a lot of data into the variable. It is advised that you efficiently check the memory of your variables while writing your code, so that you know how to deal with those variables. You can use the following code to see the memory of your objects.

- Return multiple values from Functions: This significantly helps to write simpler code rather than combining all the variables to a list or dictionary. As a best practice, you can use this tip when you have at most three or four return variables. 

- Joining strings in python: While programming in python or any other programming language, you might often come across situations wherein you would need to join one or more strings together to form a concatenated string. Fortunately, python offers a .join method using which you can concatenate all the strings from a given list. Alternatively, you can also do a loop to join the different strings in the list, however that is not considered a good design.

- Inline Documentation: While your program with python, sometimes it becomes essential to document the purpose of your code block. PEP-257 introduces a concept of using docstrings within your python code that helps you documents your methods and classes easily. 



# Python Testing Practices

> **"Untested code is broken code."** -Martin Aspeli, Philipp Von Weitershausen

So lets go through few best practices for testing our python 🐍 code:

## 1. Test in small independent chunks
* A testing unit should focus on one tiny bit of functionality and prove it correct.
* Test units need to be separate but must work altogether in any order. This implies that each test must be loaded with a fresh dataset and may have to do some cleanup afterwards. This is usually handled by `setUp()` and `tearDown()` methods.

## 2. Hook and Full test suite
* Either running a single test or a test case, when developing a function inside a module, do testing frequently.
* Running full test suite before and after every coding session ensures that you did not break anything in the rest of the code.
* It is a good idea to implement a hook that runs all tests before pushing code to a shared repository.

## 3. Naming Conventions
* Testing functions should have descriptive and self-explanatory names but, while running code we can use short names.
* The reason is testing functions are never called explicitly. 
> **For Example**: `square()` or even `sqr()` is ok in running code, but in testing code we should have names like `test_square_of_number_2()`, `test_square_negative_number()`. These function names are displayed when a test fails, and should be as descriptive as possible.

## 4. Clean and concise test sets
Code break often but when it does, with the help of good test sets, we all can rely largely upon testing suite to fix the problem or modify a given behavior. This means, testing code can be read equal or more than the running code. A unit test whose purpose is unclear is not helpful such cases.

Last but not least...
## 5. Optimization ⏰

>“Time isn't the main thing. It's the only thing.” - Miles Davis

* No single test should need more than a few milliseconds to run, this causes development to slowdown or even tests running frequency is reduced.
* For test cases based on complex data structures, which requires to load every time to run tests are heavier and requires separate test suite.
* Such separate test suites can be executed by some scheduled task, but run all other tests as frequently as needed.
***
[Refrence link for the testing best practices](https://docs.python-guide.org/writing/tests/)
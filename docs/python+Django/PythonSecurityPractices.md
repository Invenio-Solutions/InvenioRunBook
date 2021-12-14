
# Python Security Best Practices

We have mentioned 6 best practices for securing our python code:

## 1. Use the most recent version of Python
To ensure that your software works without any hinderances or doesn’t open doors for attackers, it is important to use up-to-date code.

## 2. Use a virtual environment
Don't install packages globally on your machine. Instead, use a virtual environment for each project. This is extremely benificial. For instance, if you install a package dependency with malicious code in one project, it will not affect the others. Hence, keeping each project’s packages are isolated from each other.

## 3. Set debug = false
For some Python frameworks, such as Django, debug is set to true by default in new projects. This can be helpful in development to show errors in our code, but isn’t so useful when we deploy the project to live on a server available to the public. Displaying errors in our code publicly could show a weakness in the security that may be exploited later.

When deployed live, always set the following:
Debug = false

## 4. Never commit anything with a password
Most of the developers are using GitHub these days. So double-check that you haven’t committed a file, readme, or a description of a URL with your password in it. Once committed to GitHub or a similar service, the password will always be there somewhere in a log or database for anyone to exploit it.

## 5. Beware of poisoned packages
Double-check that you’re using legitimate and updated packages. It’s possible to install packages for both Python and Node.js that have malicious code in them. Check that you have exactly the right names for each package. “00Seven” is a completely different package from "000Seven."

## 6. Keep your servers up to date
Develop a habit of checking that all your software is updated and compatible with your Python code. Random human error can destroy work that took years of planning. So make sure that the software and security management systems are up to date.

[Click here for the detailed security practices](https://www.python.org/dev/security/)

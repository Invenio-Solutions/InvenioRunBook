---
sidebar_position: 26
---

# Python Security Best Practices

We have mentioned 6 best practices for securing our python code:

## 1. Use  of the most recent version of Python

To ensure that the software works without any hinderances or doesn’t open doors for attackers, it is important to use up-to-date code.

## 2. Using  a virtual environment

Don't install packages globally on the machine. Instead, use of a virtual environment for each project is preffered. For instance, if we install a package dependency with malicious code in one project, it will not affect the others. Hence, keeping each project’s packages are isolated from each other.

## 3. Set debug = false

For some Python frameworks, such as Django, debug is set to true by default in new projects. This can be helpful in development to show errors in our code, but isn’t so useful when we deploy the project to live on a server available to the public. Displaying errors in our code publicly could show a weakness in the security that may be exploited later.

When deployed live, always set the following:
Debug = false

## 4. Never committing anything with a password

It is important that we haven’t committed a file, readme, or a description of a URL with our password in it. Once committed, the password will always be there somewhere in a log or database for anyone to exploit it.

## 5. Beware of poisoned packages

Checking that we are using legitimate and updated packages is important. It’s possible to install packages for both Python and Node.js that have malicious code in them. Checking that we have exactly the right names for each package. “00Seven” is a completely different package from "000Seven."

## 6. Keep the servers up to date

Keeping all the software updated and compatible with the Python code is important. So make sure that the software and security management systems are up to date.

***
[Click here for the detailed security practices](https://www.python.org/dev/security/)

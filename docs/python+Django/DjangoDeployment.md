---
sidebar_position: 34
---

# Django Deployment

As a Python web framework that works on the highest level, Django enables programmers to explore and create a variety of web applications. The following standards can enable the application to be production ready. 

## 1. Setting  up a robust and Consistent Database Connections:

Django provides a variety of options to create and use a database connections. PostgreSQL enables to create a strong and persitent connection. 

## 2. Enabling the Cached Loading 

The default configuration that Django uses  allows developers to use two standard loaders for templates. But each time a request is created and made to each of the two templates loaders, it automatically will search the file system and will parse the configured templates.

## 3. Storing  the Sessions in Cache

Django by its default nature stores all user sessions in the form of  databases.It is recommended that the developers leverage this and execute one or many  SQL queries in order to retrieve the user session data from its respective database and obtain the required user object information for the user. 

## 4. Keeping the Application and Libraries Separate

Django allows developers to store the application as well as the libraries in two distinct folders and make use of these folders as packages. So developers can create two folders inside the myproject folder and use them.

## 5. Storing All Templates in One Place

It is also important to store all templates as well as the template tags in the same place. You can also consider creating a Django application for containing these templates and template tags as a part of the project.

## 6. Install HTML5 Boilerplate

Developers are given the freedom to make the Django web application more responsive by making use of HTML5, CSS and JavaScript. Developers  also have the option to download as well as install the HTML5 Boilerplate. The contents of the zip file should be stored inside the templates folder.

## 7. Monitor and Control Processes using Supervisor

While deploying the respective Django application on UNIX, developers have option to monitor as well as control the processes using the help of a Supervisor. But the tool will require developers to create separate and independent configuration file for each of the processes.
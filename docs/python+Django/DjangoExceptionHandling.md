---
sidebar_position: 33
---

# Django Exception Handling

As a developer, it is apparent that a number of exceptions, errors will be encountered. It is important that these are handled at an initial stage in order to facilitate seamless application creation. 
Following must be considered in handling exceptions in Django Applications:


## 1. Django Exception classes

- AppRegistryNotReady - It occurs when the Django models are loaded before the Django app itself. This exception occurs when you are writing your own scripts and not with default Django app files.
- ObjectDoesNotExist - As the name suggests, occurs when Object does not exist.
- EmptyResultSet - Occurs when a query returns an empty set
- FieldDoesNotExist - This occurs when Field doest not exist in a model.
- MultipleObjectsReturned - This occurs when a query returns more than one result
- SuspiciousOperation - This happens when the client does something suspicious for security reasons
- PermissionDenied - Occurs when the user tries to perform a task which he is not allowed to
- ViewDoesNotExist - Occurs when Views doesnt not exist
- MiddlewareNotUsed - This occurs when particular middleware is not used in the MIDDLEWARE section of settings
- ImproperlyConfigured - This occurs when somehow, Django is improperly configured. Usually doesn’t happen when working with default Django Files.
- FieldError - Happens when there is an error in Model field
- ValidationError - Happens when Data validation fails in forms or model forms.

## 2. Django URL Resolver Exceptions

- Resolver404 - Raised by the function resolve(), a part of Django.http.Http404 library. The exception occurs when path() does not have a valid View to map.
- NoReverseMatch - This occurs when the user searches a wrong endpoint.

## 3. Django Database Exceptions

- DatabaseError - Occurs when DB is not available
- IntegrityError - This occurs when DB expects a value for a field but doesn’t get it from the user. If True, Django will store empty values as NULL in the database. Default is False.
- DataError - Occurs due to data-related issues

## 4. Django Http Exceptions

- UnreadablePostError - Occurs when a user cancels an upload.

## 5. Django Transaction Exceptions

- TransactionManagementError - This is raised for all the problems that occur due to database transactions.

# Resources: 

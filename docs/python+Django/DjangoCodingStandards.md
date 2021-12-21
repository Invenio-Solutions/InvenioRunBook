
# Django Coding Standards

Django is a Python-based web framework that facilitates quick creation of efficient web applications. 

For Python Coding Standard, refer to [this](PythonCodingStandards.md) link.



## Naming Convention
- Meaningful names must be used.
- Function and variable names must be in snake_case.
- Classnames should be in PascalCase.
- Constants must be snake_case and capitalized.

## Indentation/Space

- Use of 4 spaces for indentation is required.(Python 3 disallows mixing the use of tabs and spaces for indentation)
- Separation of top level function and classes with two blank lines is preffered.
- Separation of method definition inside the class by one line is preffered.
- There should be no trailing white spaces

## Imports

The following standards is recommneded:

- Import from Python standard library(1st)
- Import from core Django(2nd)
- Import from 3rd party vendor(3rd)
- Import from Django Apps(4th)(Current Project)
- Avoid import *

## Migrations

- Modification of the files created by makemigration command is not recommended. (do not add custom sql command)
- Placing of  custom sql command in a separate file and segreagating it from the auto generated files created from makemigration command is preffered.
- Forward and backward migration works only on auto generated files by makemigration command
- All migration cannot be reversed
- Adding of  — database=<dbConfigName> always in the migration is recommended.

    ### Forward Migration
    - python manage.py migrate appname 0002 — settings=project.settings.<Env> — database=<dbConfigName>
    - python manage.py migrate appname 0003 — settings=project.settings.<Env> — database=<dbConfigName>
    - Suppose it added all the migration 0001.py , 0002.py , 0003.py , 0004.py

    ### Backward Migration
        (Remove New migrations -0002.py , 0003.py , 0004.py)
    - python manage.py migrate appname 0001 — settings=project.settings.<Env> — database=<dbConfigName>

## Response Status

- Response message should be appended with appropriate status codes
- 200 OK — Success — GET/PUT — return resource/status message
- 201 Created — Success — POST — provide status message or return newly created object
- 204 No Content — Success — DELETE
- 304 Unchanged — Redirect — ALL — Indicates no changes since last request
- 400 Bad Request — Failure — GET/PUT/POST — invalid request, return error messages
- 401 Unauthorized — Failure — ALL — missing credentials/Authentication required
- 403 Forbidden — Failure — ALL — restricted content
- 404 Not Found — Failure — Resource not found
- 405 Method Not Allowed Failure — Failure — ALL — An invalid HTTP method was attempted

# Django Testing Practices

Testng is an important part of software development as it is an innate requirement that the errors and vulnerablities of a code are being idetified and mitigated at an very early stage. This will ensure that the code design when integrated in the production environment works efficiently. 
The following testing best practices must be followed while testing:

## Testing Best Practices

- If it can break, it should be tested. This includes models, views, forms, templates, validators, and so forth.
- Each test should generally only test one function.
- Keeping it simple is prefferable. 
- Runnning of tests whenever code is PULLed or PUSHed from the repo and in the staging environment before PUSHing to production is encouraged.
- When upgrading to a newer version of Django:
    - upgrade locally,
    - run your test suite,
    - fix bugs,
    - PUSH to the repo and staging, and then
    - test again in staging before shipping the code.

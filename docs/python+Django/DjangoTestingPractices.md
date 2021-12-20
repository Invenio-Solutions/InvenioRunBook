
# Django Testing Practices

Django is a high level framework to build scalable web applications. Django is used by companies like Google, Facebook, Pinterest, Nasa etc.

## Types of Test
**Unit Tests** Is a level of software testing where a section(unit) of an application meets the requirements, it focus on one specific function.

**Integration Tests** Is a level of software testing where individual sections are combined and tested as a group, it combined multiple pieces of code and functionality.

## Testing Best Practices
- If it can break, it should be tested. This includes models, views, forms, templates, validators, and so forth.
- Each test should generally only test one function.
- Keep it simple. You do not want to have to write tests on top of other tests.
- Run tests whenever code is PULLed or PUSHed from the repo and in the staging environment before PUSHing to production.
- When upgrading to a newer version of Django:
    - upgrade locally,
    - run your test suite,
    - fix bugs,
    - PUSH to the repo and staging, and then
    - test again in staging before shipping the code.

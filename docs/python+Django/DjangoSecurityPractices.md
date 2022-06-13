---
sidebar_position: 31
---

# Django Security Best Practices 

Django is a mature, battle-tested web framework with a well deserved reputation for security over the past 15 years. Django comes with an excellent deployment checklist that can be run on the production version of your website before deployment.

## 1. Django Version

The most recommendation security is to always be on the latest version of Django. Django has a new major release every 9 months or so (2.2, 3.0, 3.1, etc) and a minor release with security/bug fixes almost monthly (3.1.1, 3.1.2, etc). It must be updates regularly to the latest version--there is an official guide in the documentation on upgrading to a newer version--run the test suite, and carry on with the Django project.

## 2. Admin

The Django admin app is a powerful built-in feature. However, since every Django project has it located at /admin by default, it is easy for a hacker to try to force their way into any Django website at this URL. An easy way to secure your admin is to simply change the URL for the admin. 

## 3. DEBUG

Near the top of any settings file is the configuration for DEBUG. By default, it is set to True which generates, among other things, a rich and detailed error page that includes a traceback and lots of metadata including all currently defined Django settings. That is a roadmap to debugging locally, but also a guide for any hacker who wants to compromise your website if released in production. Therefore, make sure that in production DEBUG is set to False!

## 4. SECRET_KEY

The [SECRET_KEY](https://docs.djangoproject.com/en/dev/ref/settings/#std:setting-SECRET_KEY) is a randomly generated string used for cryptographic signing created whenever the startproject command is run. It is very important that SECRET_KEY actually be kept, well, secret.

All it takes is one Git commit and your SECRET_KEY is visible to anyone with access to your source code. In practice, most developers develop a working prototype of a website before adding environment variables and production configurations. Therefore, before the first deployment, take the time to generate a new SECRET_KEY. One approach is to use Python's built-in [secrets](https://docs.python.org/3/library/secrets.html) module.

## 5. ALLOWED_HOSTS

The [ALLOWED_HOSTS](https://docs.djangoproject.com/en/dev/ref/settings/#allowed-hosts) setting lists which hosts/domain names the Django site can serve. By default, it is set to the empty list, [], aka any host or domain has access to the site. This needs to be changed in production to avoid HTTP Header attacks.

For local development localhost:8000 and 127.0.0.1:8000 are commonly used in Django, therefore both should be explicitly added to the setting. And once you have a custom URL for your production location.
>A common ALLOWED_HOSTS setting for a Heroku app is therefore the following:

    # settings.py
    ALLOWED_HOSTS = ['a-random-1234.herokuapp.com', 'localhost', '127.0.0.1'] 

## 6. HTTPS/SSL
-  [HTTP Strict Transport Security (HSTS)](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) is a security policy that lets our server enforce that web browsers should only interact via HTTPS by adding a Strict-Transport-Security header. There are three implicit HSTS configurations in a settings file that need to be updated for production:
    - SECURE_HSTS_SECONDS = 0
    - SECURE_HSTS_INCLUDE_SUBDOMAINS = False
    - SECURE_HSTS_PRELOAD = False
- The SECURE_HSTS_SECONDS setting is set to 0 by default but the greater the better for security purposes. A good default is to set it to one month, 2,592,000 seconds, instead.
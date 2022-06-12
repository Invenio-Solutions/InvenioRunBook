---
sidebar_position: 3
---
# Spring Security Practices

Incorporation of security framework is enevitable for developing a reliable application. Spring has its in-built security framework that can be imbibed in the application as a starter dependency. 

The security standards that are important for an impeccable application development are as follows:

## Use of HTTPS in Production

To use HTTPS in your Spring Boot app, we need  to extend the 
`WebSecurityConfigurerAdapter` and require a secure
connection
```
@Configuration
public class WebSecurityConfig extends WebSecurityConfigurerAdapter {

 @Override
 protected void configure(HttpSecurity http) throws Exception {
   http.requiresChannel().requiresSecure();
 }
}
```
Cloud providers can greatly simplify TLS certificates. [Amazon Certificate Manager](https://aws.amazon.com/certificate-manager/) lets you provision 100% free SSL certs and handles automatic renewal, etc., 

## Test Dependencies

Tools like Synk ensures that we donot include dependencies that are subject to vulnerabilites.

* Test the app dependencies for known vulnerabilities.
* Automatically Fix issues that exist.
* Continuous Monitoring for new vulns.

## Enabling CSRF Protection

Spring Security has excellent CSRF support  by default. The usage of Spring MVC’s `<form:form>` tag or Thymeleaf and `@EnableWebSecurity`,automatically add the CSRF token as a hidden input field.  To make this part of the Spring Boot security strategy, you have to add the Spring Security starter as a dependency.

```
@EnableWebSecurity
public class WebSecurityConfig extends WebSecurityConfigurerAdapter {

   @Override
   protected void configure(HttpSecurity http) throws Exception {
       http
           .csrf()
               .csrfTokenRepository(CookieCsrfTokenRepository.withHttpOnlyFalse());
   }
}
```

## Use of OpenID Connect for Authentication

OpenID Connect (OIDC) is an OAuth 2.0 extension that provides user information. It adds an ID token in addition to an access token, as well as a /userinfo endpoint that provides additional information. It also adds an endpoint discovery feature and dynamic client registration.

## Use of  Password Hashing

Storing Passwords as plain text is never recommended considering the security of the application. Spring has an excellent provision  of encrypting the password using a symmetric encryption, key generation and hashing.

`PasswordEncoder` is the main interface for password hashing in Spring Security and looks as follows:

```
public interface PasswordEncoder {
   String encode(String rawPassword);
   boolean matches(String rawPassword, String encodedPassword);
}
```
Spring Security provides several implementations, the most popular being `BCryptPasswordEncoder` and `Pbkdf2PasswordEncoder`.
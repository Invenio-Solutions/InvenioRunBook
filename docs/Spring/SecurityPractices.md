# Spring Security Practices

Spring Boot security can mean different things. In general, it is adding the Spring Security framework to your Spring Boot web application by including the Spring Boot security starter dependency. Spring Security is an authentication and access-control framework and can be easily included in a Spring Boot application.

## Use HTTPS in Production

To use HTTPS in your Spring Boot app, extend
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
Cloud providers can greatly simplify TLS certificates. [Amazon Certificate Manager](https://aws.amazon.com/certificate-manager/) is exactly like Let’s Encrypt except it’s built into all of the AWS products/services by default. It lets you provision 100% free SSL certs and handles automatic renewal, etc., with literally zero effort/config.

## Test Dependencies

Ensure your application does not use dependencies
with known vulnerabilities. Use a tool like Snyk to:

* Test your app dependencies for known vulnerabilities.
* Automatically Fix issues that exist.
* Continuously Monitor for new vulns.

## Enable CSRF Protection

Spring Security has excellent CSRF support that’s on by default. If you’re using Spring MVC’s `<form:form>` tag or Thymeleaf and `@EnableWebSecurity`, the CSRF token will automatically be added as a hidden input field.  To make this part of your Spring Boot security strategy, you have to add the Spring Security starter as a dependency.

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

## Use OpenID Connect for Authentication

OpenID Connect (OIDC) is an OAuth 2.0 extension that provides user information. It adds an ID token in addition to an access token, as well as a /userinfo endpoint that you can get additional information from. It also adds an endpoint discovery feature and dynamic client registration.

## Use Password Hashing

Storing passwords in plain text is one of the worst things you can do for the security of your app. Luckily, Spring Security doesn’t allow plain text passwords by default. It also ships with a crypto module you can use for symmetric encryption, key generation, and password hashing (a.k.a., password encoding).

`PasswordEncoder` is the main interface for password hashing in Spring Security and looks as follows:

```
public interface PasswordEncoder {
   String encode(String rawPassword);
   boolean matches(String rawPassword, String encodedPassword);
}
```
Spring Security provides several implementations, the most popular being `BCryptPasswordEncoder` and `Pbkdf2PasswordEncoder`.
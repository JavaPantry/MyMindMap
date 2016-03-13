# Spring Security

Eugen Paraschiv

**NOTE:** Use github code version instead code from udemy site

- [Course source code on github](https://github.com/eugenp/course)
- downloaded to workspace c:\SpringSecurityCourse_Workspace\course-master.zip
- [Project home page](http://localhost:8080/spring-security/)
- Course uses [Mustache framework](https://github.com/janl/mustache.js)




## Section: 1 - Spring Security Setup
- Lecture 1: Introduction to the Course
- Lecture 2: The Spring Security Setup and Form-based Authentication

```js
SEVERE Exception sending context initialized event to listener instance of class org.springframework.web.context.ContextLoaderListener
org.springframework.beans.factory.parsing.BeanDefinitionParsingException: Configuration problem: No AuthenticationEntryPoint could be established. Please make sure you have a login mechanism configured through the namespace (such as form-login) or specify a custom AuthenticationEntryPoint with the 'entry-point-ref' attribute 
To fix 
Add to src/main/resources/webSecurityConfig.xml
<form-login/>
```

```js
Run time csrf error
To fix Add to src/main/resources/webSecurityConfig.xml <br/>
<csrf disabled="true"/>
```

```js
HTTP Status 404 - /spring-security/j_spring_security_check
instead http://localhost:8080/spring-security/login.html
use http://localhost:8080/spring-security/login
```

-- fixed course project C:\SpringSecurityCourse_Workspace\s1_vid2 


- Lecture 3: Authentication – Log in and Log Out
- Lecture 4: Authorization – URL

-- C:\SpringSecurityCourse_Workspace\s1_vid2vid4 copied&merged from s1_vid2

- Lecture 5: Authorization – Security Expressions
- Lecture 6: Authorization – in Page

## Section: 2 - Registration
- Lecture 7: The Registration Process with an In-memory Authentication Provider
- Lecture 8: The Registration Process with a JDBC-backed Authentication Provider
- Lecture 9: The Registration and Authentication Process with JPA

## Section: 3 - The Remember Me Authentication
- Lecture 10: The Remember Me Mechanism with a Cookie - The Basic Setup
- Lecture 11: The Remember Me Mechanism with a Cookie - Advanced Analysis
- Lecture 12: The Remember Me Mechanism with Persistence
- Lecture 13: The Remember Me Mechanism with More Advanced Scenarios

## Section: 4 - Spring Security with LDAP
- Lecture 14: Authentication with LDAP
- Lecture 15: Authorization with LDAP
- Lecture 16: Authentication and Authorization with an External LDAP Server

## Section: 5 - Authorization with Spring Expressions
- Lecture 17: Authorization With Expressions - URL
- Lecture 18: Authorization With Expressions - in Page
- Lecture 19: Authorization With Expressions - on Methods

## Section: 6 - REST Authentication and Authorization
- Lecture 20: The REST Service and Its Setup
- Lecture 21: REST with Basic Authentication
- Lecture 22: REST with Digest Authentication

## Section: 7 - Spring Security ACL
- Lecture 23: Introduction to Domain Object Security and ACL
- Lecture 24: The ACL Data Structure
- Lecture 25: The ACL Setup and Configuration with Spring Security
- Lecture 26: Advanced ACL


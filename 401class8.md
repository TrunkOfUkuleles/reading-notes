

### QUESTIONS

1. When is Basic Authorization used vs. Bearer Authorization?
    basic auth the process of login authentication. Once that happens, the server can send a token back. That token is used for persistant state bearer authorization.
2. What does the JSON Web Token package do?
    the JWT package gives you the methods to generate a token using an input string and a secret. The secret bit can never be decoded, but a commpare function allows a boolean check.
3. What considerations should we make when creating and storing a SECRET?
    secret is going to be set by the front end. Similar to ports, an ENV is probably a good idea.

### Vocabulary

encryption: method of converting information via a method that can be decrypted by the owner/app
token: generated persistant peice of information that makes keeping state way easier
bearer:  (header.authorization) token field when submitting
secret: the key used to generate the token 
JSON Web Token: Said token - generated from a method in the package

## Preview

Which 3 things had you heard about previously and now have better clarity on?
    encryption, token usage
Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    getting the flow of encryption - that can get messy. 
What are you most excited about trying to implement or see how it works?
    rebuilding it all and feel like it is easier. 

### RBAC
    Role Based Access Control is a organizational strategy that has different layers of access depending on different roles in a system. 

## Process 
    - inventory your systems
    - analize workforce and build roles
    - asign roles
    - stick to system
    - review periodically

![RBAC]{'./assets/Role-based_access_control.jpg'}


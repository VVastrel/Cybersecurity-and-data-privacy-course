# Reflections

Here are some short reflections on the labs I've completed on Portswigger.net

### SQL injection vulnerability in WHERE clause allowing retrieval of hidden data

Learned how easy it is to spot and take advantage of vulnerabilities in SQL databases, and how to use intercept feature in Burp to reveal hidden values. Had some trouble configuring Burp to intercept my preferred browser so decided to just stick to using the recommended chromium.

### SQL injection vulnerability allowing login bypass

It's apparently ridiculously easy to login as admin on sites that have poor security. Changing the username parameter to admin and logging in as an admin didn't give me any trouble.

### Username enumeration via different responses

This one was all about finding the POST /login request, using the HTTP history -feature and using the Burp Intruder to go through usernames and passwords to find the right combination that let me log in. Had some trouble doing everything in the right order.

###  Password reset broken logic

In this lab I learned that once an attacker has an access to ones email account, it's easy to change the password of the accounts linked to that email, using a password reset functionality. Once again I used HTTP history to check the POST request and find the reset token, which then allowed me to change the username and password of the target account.

### Unprotected admin functionality

In this lab I accessed an unprotected .txt file with the address bar and gained information on how to access the administrator panel and delete carlos from the site. Very straightforward. Didn't have any issues here. 

### User role can be modified in user profile

Here, once again, Carlos has slighted us and we must retaliate by deleting his account from the site. Using HTTP history -feature in Burp, I gain access to POST requests that let me manipulate my users roleid, and elevate it to a higher one, that then lets me gain admin priviledges. As an admin I delete Carlos's account. He deserved it.

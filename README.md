# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: Session hijacking

<img src="https://github.com/mattcc1398/Week8/blob/master/Blue%20SH.gif" width="800">

For hijacking, we first log in on one browser (Chrome), and then use the PHP session ID tool to get the session ID. We then change the session ID in the second browser (Firefox) to that session ID, which allows us to bypass having to enter a username and password.

Vulnerability #2: SQLI

<img src="https://github.com/mattcc1398/Week8/blob/master/Blue%20SQLI.gif" width="800">

Show a salesperson, and then enter a SQL injection into the id field of the URL.


## Green

Vulnerability #1: XSS

<img src="https://github.com/mattcc1398/Week8/blob/master/Green%20XSS.gif" width="800">

Leave feedback with XSS in the message, and the script will run when you log in and view the feedback.

Vulnerability #2: Password enumeration

<img src="https://github.com/mattcc1398/Week8/blob/master/Green%20PE.gif" width="800">

The system indicates whether or not the username is valid with the bolding of the "Log in was unsuccessful" text. Bold text means the username is valid, and non-bold means the username is not valid. 

## Red

Vulnerability #1: CSRF

<img src="https://github.com/mattcc1398/Week8/blob/master/Red%20CSRF.gif" width="800">

Go to edit a user, inspect element, change CSRF token, and then edit a field. The change will be applied even though it shouldn't be.

Vulnerability #2: IDOR

<img src="https://github.com/mattcc1398/Week8/blob/master/Red%20IDOR.gif" width="800">

Go to the public site, click find a salesperson, and change ID=10.

## Notes

Describe any challenges encountered while doing the work

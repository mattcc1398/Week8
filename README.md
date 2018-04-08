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

<script>alert('Mallory found the XSS!');</script>

Vulnerability #2: Password enumeration


## Red

Vulnerability #1: CSRF

Go to edit a user, inspect element, change CSRF token, and then edit field (change will be applied)

Vulnerability #2: IDOR
Go to public site, click find a salesperson, change ID=10


## Notes

Describe any challenges encountered while doing the work

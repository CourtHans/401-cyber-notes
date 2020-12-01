# Day 39 - SQL with Burp Suite, WebGoat
11/30/20

* [Understanding SQL Injection, Identification and Prevention](https://www.varonis.com/blog/sql-injection-identification-and-prevention-part-1/)

> "SQL Injection attacks are one of those situations where the outcome can be wildly disproportionate to the amount of effort that went into executing it."

"Standardized query language (SQL) is, in one form or another, still the dominant method of inserting, filtering and retrieving information from a database." Underestimating a database's "power and complexity" can lead to many of the security issues that occur when you put a web application in front of a SQL database. It's useful to mentally sub in the word "command" every time you hear "query."

The basics of the language haven't changed much since its invention (in the 1970s). 

**CRUD**
* Create
* Read
* Update
* Delete

Insert, Update, Select, Delete, From, Where are common query words.

"Doing string concatenation of SQL statements is the fastest road to having your site and application owned."

"In general, web frameworks prevent SQL injection attacks by providing easy methods of data querying so that developers aren’t seduced into writing hideously vulnerable SQL string concatenation statements" with two primary methods: user input sanitization and syntax provision.

Where you can add additional security layers:

**Database**
* Sufficient and appropriate database user permissions set
* Extraneous or unused database features disabled
* Database logging enabled
* Database backup / restore procedure
* Database connection filtering procedures enabled (example: MySQL has options to prevent execution of multiple SQL statements in a single query)
* Database drivers up to date

**Application**
* Using filtering options
* Using parameterization options
* Using DB calls only when needed? (Could you use a static site generator?)
* Code lint/checks for potential SQL injection points
* Manual check for SQL Injection prone points
* Application logging

**Web Server / Web Firewall**
* Use WAF SQL Injection pre-filters
* Rate limit to prevent mass SQL Injection attempts
* Alert on SQL Injection pattern attempts




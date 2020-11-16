# Day 32 - XSS, SQL Injection
11/17/20

* [SQL injection and XSS: what white hat hackers know about trusting user input](https://www.freecodecamp.org/news/sql-injection-and-xss-what-white-hat-hackers-know-about-trusting-user-input/)

***"Usually, the weakest point in the security of your software is you."***

"Malicious actors may be able to send SQL commands that affect your application through some input on your site, like a search box that pulls results from your database. Sites coded in PHP can be especially susceptible to these, and a successful SQL attack can be devastating..."

"The following payloads can be used to test inputs:</br>
`' OR 1='1` evaluates to a constant true, and when successful, returns all rows in the table.</br>
`' AND 0='1` evaluates to a constant false, and when successful, returns no rows.</br>

The main rule of protecting against SQL injection is ***don't trust user input***.

Methods to safely abstract SQL queries from user input:
1. Prepared statements with variable binding (or parameterized queries),
2. Stored procedures; and
3. Whitelisting or escaping user input.

"Cross Site Scripting attacks, or XSS, occur when JavaScript code is injected into a web page and changes that page’s behavior." It comes in "three flavors" and the differences amount to where the attack payload is injected into the application.
1. DOM (Document Object Model) based
2. stored
3. reflected XSS

DOM based XSS occurs when a JavaScript payload affects the structure, behavior, or content of the web page the user has loaded in their browser. 

Stored XSS occurs when the attack payload is stored on the server, such as in a database. The attack affects a victim whenever that stored data is retrieved and rendered in the browser. 

Reflected XSS similarly occurs when the injected payload travels to the server, however, the malicious code does not end up stored in a database. It is instead immediately returned to the browser by the web application.

Questions to ask about your application:
* How does data flow through our application?
* What does a user expect to happen when they interact with this input?
* Where on our page does data appear? Does it become embedded in a string or an attribute?

Sample payloads:
* `"><h1>test</h1>`
* `'+alert(1)+'`
* `"onmouserover="alert(1)`
* `http://"onmouseover="alert(1)`


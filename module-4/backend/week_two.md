## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6? 

The way one declares a class/constructor function. I'm converted to Es6. I love js classes <3

2. What's the difference between asynchronous and synchronous JavaScript? 

Synchronous javascript executes one command at a time, in order. Asycnchronous javascript starts to execute a command, and then starts the next command. When the asynchronous command is completed, it reenters the queue to be completed.

3. What are the four pillars of Object Oriented programming?

Abstraction Polymorphic Inheritance Encapsulation (Thanks for the lighting talk, Ben Jacobs!)

4. What are some tools available in JavaScript to help you write object oriented code?

Classes, Static functions, Prototype functions, call back functions

5. What are some key concepts to be aware of when refactoring your JavaScript?

Single responsibility. Object oriented. Readability. Also, all the pillars.

6. What's a callback function and what are some reasons when we use/need callback functions?

A function passed into another function as an argument. We'd use them when we want to explicitly determine the order the functions are exected (i.e. the call back function would not be executed until the parent function was executed). Also, to keep code dry.

7. What's the scope of variables in Javascript?

local variables are available within functions, global variables are available outside of individual functions

8. What's the difference between `==` and `===` in JavaScript?

=== doesn't do a type conversion before checking for equality, so the type has to already be the same for it to find equality

9. Why do front end frameworks exist?

To organize sprawling code and wrangle large amounts of data.

#### Review  

10. Why do people say "HTTP is stateless"?

HTTP has no memory of what is sent before and after in other HTTP requests or responses.

11. Describe a RESTful API.

A RESTful API includes predictable CRUD routes: index, show, update, create, and delete 

12. What are some main characteristics of a team following an agile workflow?

Performs iteratively, frequent communication with stakeholders/product owners, standups!, flexibility of design (you never know as little about a project as when you first start) 

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?

Advantages: let someone else handle security, user convenience. Disadvantages: someone else is in control of the mechanism for your customers to log in, users are giving up a lot of privacy, if users don't have an account with the relevant company, it's an extra step to create an account, someone else is handling (or perhaps mishandling) your security. 

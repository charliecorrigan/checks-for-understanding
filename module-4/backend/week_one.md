## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 


#### Review  
12. What's the MVC design pattern? Describe each part of MVC.
13. What are a few ways to optimize a Rails application?
14. What's a background worker? When would we want to use a background worker?


1. What's the most useful thing you learned from completing the intermission week work?

I enjoyed doing Sorting Suite. I got a lot more comfortable with Javascript/Chai getting to play with it in a familiar context. It helped me to understand a lot of the similarities between Javascript and Ruby, which helps to isolate the differences.

2. What are some tools to help debug JavaScript code?

Debugger is my favorite. There's also console.log and pry

3. What are some tools you need in order to unit test your JavaScript?

We've used Chai so far and are just getting started using Selenium. I'm not comfortabe with Selenium yet, but hopefully I will be by the time I get through Quantified Self.

4. What is the syntax for invoking a function?

myFunction()

5. What is CORS?
Cross-Origin Resource Sharing, but I don't realy know much about it

6. How do we enable CORS?

Not sure. I could proable google it, but that might defeat the purpose of the check for understanding. I imagine there's a configuration setting to change though.

7. What's `this` in JavaScript?

`this` is a pointer that isolates the specific instance of an object or element to act upon. It is defined by its context.

8. What is Webpack and why is it useful?

Webpack manages our CSS, SCSS, Javascript, and other dependencies and assets. It precompiles, and I'm pretty sure it minifies/uglifies the files as well. It keeps the code cleaner and wrangles files.

9. When/why do you want to use event delegation?

Event delegation is useful when we want to utilize a DOM element that doesn't exist when the page is initially loaded/when the Javascript is originally run. It allows us to anchor the event to an element that will exist and then narrow down our target at the time the event happens, rather than on page load.

10. What is a callback function?

A callback function is a function that is passed as an argument in another function to be called from a nested position.

11. What's `npm` and what do we use it for?

npm is Node Package Manager and it helps to install libraries.

#### Review  
11. What's the MVC design pattern? Describe each part of MVC?

MVC is Model, View, Controller. The controller manages routes and acts as a laison between the view and the model, passing data between them as needed. The view is the client-facing elements on a web app. The model is where logic is handled, where data is manipulated as needed, and communicates with the database.

12. What is AJAX? What are some benefits of using AJAX?

AJAX is Asynchronous Javascript and XML. AJAX calls can communicate with the server side of an app asynchronously, sending and receiving HTTP requests and responses without reloading the entire page. Because it's loading smaller components, it's faster than reloading the entire page for every request.

13. What are a few ways to optimize a Rails application?

Background workers, caching, refactoring queries

13. What's a background worker? When would we want to use a background worker?

Background workers are processes set to run on their own thread. It's a sort of asynchronous process and is useful when the job assigned to a background worker is time-consuming and would interfere with the load time of a page.

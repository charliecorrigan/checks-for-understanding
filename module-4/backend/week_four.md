## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's your favorite project management tool? 

Waffle -- the UX is a lot cleaner than Pivotal Tracker and it's more fun to move the card through the different stages of completion.


2. Why do we create staging environments?

To try out our code in an environment that more closely mimics production than development would.

3. What are the characteristics of a good README (in your opinion)?

Clear, thorough, organized, assume reader knows nothing, use code snippets. Very similar to a good lesson plan.

4. What's one main improvement you're going to make to your code regarding accessibility issues?

Use more semantic tags. I used them frequently before Turing, but have gotten into the habit of wrapping everything in divs and ignoring most other tag options.

5. What are some basic security concerns to be aware of when building applications?

Cross site scripting, pivilege escalation, mass assignment, predictability of user ids, http instead of https. SANITIZE INPUTS.

6. Why is continuous integration helpful/important?

Ensures tests are passing before merging changes into code base, prevents app-breaking errors from making it into development or master, gives developer a heads up about issues they perhaps didn't notice before pushing, helps to keep development and master clean and functional.

7. What are some continuous integration tools?

TravisCI

#### Review  

8. What are some characteristics of "good" git workflow?

I'm learning that this is different in different companies. But, for me at Turing -- commit frequently, pull from master frequently, write detailed pull requests, review others' code thoroughly before merging, leave helpful comments, and keep the master branch clean

9. What are the four fundamental concepts of object oriented programming?

Polymorphism, Encapsulation, Abstraction, and Inheritance

10. What's a module in Ruby and what's the difference between a class and a module?


Modules and their methods are accessible across any classes that include them, classes are instantiatied as objects, modules aren't -- they're a namespace 

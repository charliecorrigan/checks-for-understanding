## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?

Node is a platform for running server-side Javascript. It runs on v8.

2. What is Express? Why is Express similar to in the Ruby world?

Express is a lightweight Javascript framework, similar to Ruby's Sinatra.

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

```
app.get(url, (request, response) => {
  response.json(stuff)
)}
```
PS. I admit that I had to look at my notes to remember the syntax for this. I haven't memorized it yet. I'm hoping using Express for my capstone will help commit this stuff to my working memory.

4. What do we use Knex for?

To interface with a database in Node. We've used it for postgresql... I wonder if it's the same for other databases?

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

Move routes into their own files in a controller folder. Move logic out of the routes and into files in a model folder. The view is already separated out into its own repo.

6. How do you execute raw SQL in node?

knex.raw("INSERT SQL STUFF HERE")

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

Organizations do this so that they can run apps on different platforms without having to reinvent the backend of the app each time. It provides a pretty clear separation between the Models/Controllers and the View of MVC apps. Not sure what the disadvantages are. To me, the disadvantage is that it seems harder and less familiar, but that seems like a short-sighted thing to list as a disadvantage.

#### Review  

8. Describe DNS.
DNS is the Domain Name System, which associates IP addresses with more human-readable addresses -- such as www.google.com or www.charlispscorrigan.com. When you type in a web address (a domain name), a DNS server looks up and returns the IP address associated with that domain name. Then your browser can route your HTTP request to the right IP address.

9. What does writing clean code mean to you?

Writing clean code involves:
* Writing single responsibility components
* Using appropriate vocabulary (i.e. selecting the right enum instead of using each for everything)
* Managing white space and indentations
* Organizing code architecture according to OOP principles
Writing clean code results in being able to write more complex programs with less confusion for yourself, your colleagues, and future code-maintainers

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

HOTEL -- user should be able to reserve a room. That room reservation should have date information associated with it so that there are no double bookings... Since a user/guest could book many rooms and a room could be booked by many users (on different dates), I'd probably start with a Guest class, a Room class, and a Reservation class that is a joins table between rooms and guests. A room class would keep a list of it's attributes (bed size, outdoor area, other amenities, possibly regular rate), a guest class would hold onto saved user attributes (contact info), and a reservation would have the room id, the user id, and info specific to the reservation: the reservation dates, price, discounts, special requests, etc)


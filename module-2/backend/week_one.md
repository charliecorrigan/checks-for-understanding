## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

- GET: gets stuff to display
- PUT: updates content?
- POST: Creates content?
- DELETE: deletes content
- Not sure what #5 is. We haven't used it yet.

2. What is Sinatra? 

- A framework that helps to navigate interractions between Ruby and the web.

4. What is MVC? 

- Model, View, Controller

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes? 

- Probably because labels carry information about intent, so even if it will work with the wrong label, it ought to be labeled properly so that others can navigate/fix/understand what you've created

6. What types of variables are accessible in our view templates without explicitly passing them? 

- instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

- No idea
  
9. What's the purpose of ERB?

- To generate dynamic pages

10. Why do I need a development AND test database?

- to preserve integrity of data

11. What's responsive design?

- sites that adjust to screen size for readability

12. What is CRUD and why is it important?

- Create, Read, Update, Delete. It's the four main tasks expected in user/databsae relations

13. What does HTTP stand for? 

- Hyper text transfer protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

- <% ruby stuff %> This executes code and doesn't display it
- <%= ruby stuff %> This executes code and displays the evaluated value

15. What's an ORM?

- Object relational mapping. Thinking of or executing or managing relational databases/tables in an object oriented way

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?

- Active Record

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

```
#READ - display all restaurants
get '/restaurants' do
end

#READ - display one restaurant
get '/restaurants/:id' do
end

#CREATE - display create new restaurant form
get '/restaurants/new' do
end

#CREATE - saves new restaurant into restaurant database, redirects to view new restaurant record
post '/restaurants/:id' do
end

#UPDATE - display edit restaurant form
get '/restaurants/:id/edit' do
end

#UPDATE - saves edited restaurant info in database and displays edited retaurant
put '/restaurants/:id' do
end

#DELETE - deletes selected record and redirects to index
delete '/restaurants' do
end
```
18. What's a migration? 

- instructions for changing an existing database

19. When you create a migration, does it automatically modify your database?

- No. must run `rake :db:migrate`

20. How does a model relate to a database?

- Models are the category of the program that interacts directly with databases

21. What's the difference between agile workflow and waterfall method?

- Agile completes a project through a series of iterations that produce multiple working but incomplete versions of the program. Waterfall completes all functionality at once.

22. What is the difference between `#new` and `#create`?

- #new temporarily holds onto intitialization information. It doesn't post to the database without #save. Create immediately creates a new database record.

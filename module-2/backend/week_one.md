## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  -get: sends request; finds specific URI
  -post: allows you to create a new instance in your data
  -delete: destroys data
  -PUT: allows you to update or replace a certain element in a database
  -PATCH: like put, it also allows you to update a certain element in a database    

2. What is Sinatra?
  - Sinatra is a framework; a DSL language that allows us to manipulate code by eliminating extra work that’s automatically taken care of in the background. 

4. What is MVC?
  - Model, View, Control: These are sub folders that live within our app parent folder. A framework that allows you to build apps in a manner that is convention.

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  -There is a order of precedence, plus most programmers are used to using a specific form of programming. 

6. What types of variables are accessible in our view templates without explicitly passing them?
  -Instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  - name = ‘Mr. Ed’ 
  - :locals => {name: name}

9. What's the purpose of ERB?
  - Embedded Ruby (ERB), allows you to add ruby code into html files

10. Why do I need a development AND test database?
  - You need a development and test database to be able to build your app without effecting your production database. Having both also allows you to use similar data to help build your app.

11. What is CRUD and why is it important?
  - Create, Read, Update, Destroy: these are the basic functions that guide and help build our app.

12. What does HTTP stand for? 
  - Hyper Text Transfer Protocol

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  - <%= %> and <% %>, one “prints” what you wanna see from a user view, the other doesn’t output

14. What's an ORM?
  - Object Relational Mapping- allows you to manipulate objects between databases.

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  - Active Record

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  - GET/restaurants  — takes you to the index/dashboard
  - GET/restaurants/new — uses the HTML form to create new instance  
  - POST/restaurants —  create a new restaurant instance 
  - GET/restaurants/id — shows an instance of a restaurant 
  - GET/restaurants/id/edit — uses HTML form to edit instance
  - DELETE/restaurants/id — deletes an instance using HTML form

17. What's a migration? 
  Allows you to create a schema in with ruby, to build your "blueprint" for you database.

18. When you create a migration, does it automatically modify your database?
  - Unless you run “rake db:migrate” after you build the instructions for how you want to schema to look and add a change to a schema, then no.

19. How does a model relate to a database?
  - The model uses the database to pull data and with it add functionality to your app.

20. What is the difference between `#new` and `#create`?
  - Although new creates a new instance(row), it doesn’t save it back into your database unless you use the .save method, create does both.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  - Use the for_each method and include the header options, iterate through the rows and use the .create!(row.to_has) method. Then run rake db:seed

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']} 
}
```
How would I add 'granola bar' to things you should have when hiking?
  - activities[:hiking][:supplies] << 'granola bar'

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  -Encapsulation - hide what you don't want others to see, keep state and logic internal
  -Abstraction - the representation of an object, hiding the complexity of actions into simple verbs
  -Inheritance - a relationship between two objects, giving the "child" class the state and behaivior of the parent class
  -Polymorphism - the condition of occuring in several different forms


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

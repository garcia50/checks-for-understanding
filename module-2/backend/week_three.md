## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
- rails new movie_mania -T -d="postgresql" --skip-turbolinks --skip-spring

2. What do Models generally inherit from in rails?
- ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
- ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
- resources :horses, only: [:show] 

5. What rake task is useful when looking at routes, and what information does it give you?
- rake routes/rails routes; It provides the prefix, verb, URI pattern and Controller#Action

6. What is an example of a ????route helper???? When would you use them?
- Path Helper????...like a route path help...like companies_path instead of "/company/1"
I would use them to define a path/direction I'd like a certain action or link to visit.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
- _url will return the entire url path, while _path will only return the specific uri path

8. What are strong params and why are they necessary?
- Stong Params is how your app and rails ensures security from malicious people that can damage your app. The strong params will only allow/permit the params you permit into your application. For example, a form can and will only except string as suppose to integers or other data types. 

9. What role does `form_for` play in helping us create our forms?
- form_for is a pre-existing helper method/feature that allows an app to collect user input that runs through the new/create controller. Its a "form" that allows users to either create or update data.

10. How does `form_for` know where to submit the user's input?
- rails magic!!!!   jk...rails knows if it should be a new or update based on what you are asking it what to do in your Controller action.

11. Create a form using a `form_for` helper to create a new `Horse`. 
- <%= form_for @horse do |f| %>
    
    <%= f.label :breed %>
    <%= f.text_field %>

    <%= f.submit %>
  <% end %>

12. Why do we want to validate our models?
- To ensure that a user can create/save data in the database if they provide the necessary attributes to create the record.











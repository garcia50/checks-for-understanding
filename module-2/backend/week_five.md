Questions from Week 5:
1. How do we make flash messages display on a page?
-In the layout application.html file include:
    <% flash.each do |type, message| %>
      <%= content_tag :div, message, class: type %>
    <% end %>
    then in your controller action: flash[:notice] = "message"

2. Where is cart information/temporary information usually stored?
- Client side, from within the session.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
- Space is the main reason. You would persist info if say a user logs out after storing items in a cart, then logs out, you would want them to be able to log back in and find whatever was previously recorded.

4. What is the purpose of the asset pipeline?
- The purpose of the asset pipeline is to be able to compile data/info that can be easily transferred and translated between different servers and browsers.

5. Why do we precompile our assets?
- We precompile to that whatever browser your using can store and save caches so save loading time when a user revisits a certain page. 

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
  - links a specific style sheet specified to whatever css attached to it.
<%= javascript_include_tag "application" %>
- links a specific javascript style sheet specified to whatever css attached to it.
<%= image_tag "rails.png" %>
- links to a specific image and is able to be rendered.
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
- How to instal, Clear title/description(what is it for), Quirks of usage(dev vs prod, common issues), Links to relevant documentation, Index, Schema. 
-The benifits would be for a stranger to be able to know exactly how the project works and to know exactly how it is currently built. 

8. What are the top four accessibility issues that we as developers should be aware of?
- audio impairment, mobility, visual impairment, color-blindness

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
- callback. We would find it within our controllers

10. Given the following object, how would we create a scope for all users who are active?
```ruby 
User.create(name: "Happy", active: true)
```
-implementing a role

11. What is the difference between a scope and a class method?
- Scopes allows you to return simple and specific objects, whereas class methods can also return specific object but it also allows you to transfer logic from one class to another. 

Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  - given[:cart]["48"] = 4
  12b. How would you increase the quantity of item 29?  
  - given[:cart]["29"] += increase_amount
  12c. How would you find out how many items your user is thinking about purchasing? 
  -given[:cart].values.sum  
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  

## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  - Active Record is a ruby library that helps you build apps in conjunction with frameworks such as Sinatra; it translates ruby code into sql queries and has many predefined methods that help "speed up" production by eliminating extra code one would have to write.

2. Assume you have the following model:
  

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
- You can call .all, .find, .find_by, etc. I have access to them by inheriting through 'ActiveRecord' and the 'Base' library that has been pre-set for me.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

 - team = Team.find(4)
   team.name
   team.owner_id



4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
- team.find(4)
- team.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
- Teacher has_many Students
  Students belong_to Teacher 

6. Define foreign key, primary key, and schema.
- Foreign key is a unique key id that represents its origin table and is used to connect data through different tables. 
- A primary key is a unique identifier that represents an object(row) in a table.
- A schema is  a "certificate of verification" or a "blue print" of how the database is structured.

7. Describe the relationship between a foreign key on one table and a primary key on another table.
- Both keys represent the same object, one is located in the origin table, the other is located in another table to link related/inquired data.

8. What are the parts of an HTTP response?
-  Status code, Header, and an optional body.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources 

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week

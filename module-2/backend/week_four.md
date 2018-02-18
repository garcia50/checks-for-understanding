## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  -A cookie is data stored on a users computer(or depending on the app/server) that is remembered by the browser.

2. What’s the difference between a session and a cookie?
  -The diiference is that once you close a session for any current_user/athentication gets deleted whereas a cookie saves any info thats not secure sensitive(unless commanded to) and stores it in memory.

3. What’s a flash and when do you want to use flashes?
  -A flash is a name value pair that you can add to your app throughout a session and prompt messages to a user.

4. Why do people say “HTTP is stateless”?
  -It's stateless because the connection between the browser and the server is lost once the transaction ends.

5. What’s authentication? Explain.
  -Authentication is proving a user says who they say they are.

6. What’s the difference between authentication and authorization?
  -The difference is access versus control. Authentication verifies a user, while authorization controls the permmissions and access they have.

7. What’s a before filter?
  -helps keep our controller actions clean by removing authentication and authorization logic out. Before any actions run the before filter will check that the current_user has access to all or specfic controller actions.

8. How do we keep track of a user once they’ve logged in?
  -Sessions, current_user and COOKIES!

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  - When you don't need the entity that a regular resource provides; for example when you simply want to nest admin controllers within an admin file from within your controllers and have a route that allows you to access those actions/routes.

10. At a high level, what tools can you use to implement authorization? How would you use them?
  -You can use the helper methods, setup roles with enum for specific users to give them special control, there's also namespacing that separates the roles of a authorized user to that of a regular user. 

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum? 
  -An enum is essentially a method that iterates through an array and assigns different behaivior for specific users. You declare it in your models.

12. What are some strategies you can use to keep your views DRY?
  -Use partial forms, using SASS selectors, making sure you keep most if not all your logic in your models.


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
{holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
{holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
{holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```
new_array = given.map do |holiday|
  holiday[:holiday][:name]
end.sort 

new_array.each { |name| print "#{name }"" }

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 
.to_i


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

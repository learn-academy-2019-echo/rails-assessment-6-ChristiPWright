# ASSESSMENT 5: INTRO TO RAILS
## Interview Practice Questions

Answer the following questions. First, without external resources. Challenge yourself to answer from memory. Then, research the question to expand on your answer. Even if you feel you have answered the question completely on your own there is always something more to learn.

1. MVC (Model View Controller) is a pattern for the architecture of a software program. Give a brief description of each component and describe how Ruby on Rails handles MVC.

  Your answer: Controller traffic cop; Model is the data/table structure; View is the view/user interface

  Researched answer:
I stick with my original answer.
https://medium.com/the-renaissance-developer/ruby-on-rails-http-mvc-and-routes-f02215a46a84

2. Using the information given, fill in the blanks to complete the steps for creating a new view in a Rails application.

  Step 1: Create the ____route_____ in the file config/routes.rb
  ```
  get '/about' => 'statics#about'
  ```

  Step 2: Create the ______controller______ in the file ___static_controller.rb__
  ```
  class __StaticController__ < ApplicationController
    def _about__
      render ___html: "hello"___
    end
  end
  ```

  Step 3: Create the View in the file ___about.html.erb___________
  code:
  ```
  <div>This is the About page!</div>
  ```


3a. Consider the Rails routes below. Describe the responsibility of  each route.
##each route establishes a path between the users page and its controllers method

/users/       method="GET"     # :controller => 'users', :action => 'index' ##displays all users

/users/1      method="GET"     # :controller => 'users', :action => 'show' ## displays one user

/users/new    method="GET"     # :controller => 'users', :action => 'new' ##displays form to create new user

/users/       method="POST"    # :controller => 'users', :action => 'create' ## creates new user

/users/1/edit method="GET"     # :controller => 'users', :action => 'edit' ##updates/edits an exisiting user

/users/1      method="PUT"     # :controller => 'users', :action => 'update' ##return an html form for editiing a user

/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy' ##delets the user



3b. Which of the above routes must always be passed params and why?

the ones that have one after them because you are operating on a specific user


4. What is the public folder used for in Rails?

  Your answer: idk

  Researched answer:
Contains the common files for any web applications that are publicly available. "Dumb" files that don't interact with the backend like homepages.


5. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

get '/game/:guess' => 'main#game'


6. In an html form, what does the "action" attribute tell you about the form? How do you designate the HTTP verb for the form?

  Your answer: ...

  Researched answer:
where to send the data
Ex. <form action="URL">
https://www.geeksforgeeks.org/html-action-attribute/

7. Name two rails generator commands and what files they create:

  Your answer: ...

  Researched answer:
  rails generate resource => creates everything a generating model deos as well as creating the routes file
  
  rails destroy resource => goes through every path that a generator uses to create a file byt removes the file
  
  https://medium.com/@josephdlawson21/using-the-generate-command-in-rails-9c738380f2d9

8. Rails has a great community and lots of free tutorials to help you learn. Choose one of these resources and look through the material for 10-15 min. List three new things you learned about Rails:
- **[Ruby on Rails Tutorial](https://www.tutorialspoint.com/ruby-on-rails/index.htm)
- [Rails for Zombies](http://railsforzombies.org)
- [Rails Guides](http://guides.rubyonrails.org/getting_started.html)

1."app/helpers: The helpers subdirectory holds any helper classes used to assist
the model, view, and controller classes. This helps to keep the model, view, and
controller code small, focused, and uncluttered." pg 16 
helper classes |do| extract some logic complexity out of the view & make it easier to test the logic <https://mixandgo.com/learn/the-beginners-guide-to-rails-helpers>

2."doc: Ruby has a framework, called RubyDoc, that can automatically generate
documentation for code you create. You can assist RubyDoc with comments in
your code. This directory holds all the RubyDoc-generated Rails and application
documentation." pg 16 - no clue this existed

3. logfile - creates scripts to manage the various error logs

9. STRETCH: What are cookies? What is the difference between a session and a cookie?

  Your answer:smaller set of datastorage for user interactions

  Researched answer
  small piece of data sent from a website and is stored on the user's computer by the user's web browser which is helpful for things like keeping your website's shopping cart active. 
  
  https://en.wikipedia.org/wiki/HTTP_cookie
  https://us.norton.com/internetsecurity-privacy-what-are-cookies.html

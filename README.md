# Ignition2015_week5
Diving deeper in the MVC aspects of Rails

# Week 5: Rails MVC

#### Required 
1. Read the [Odin Project Routing Guide](http://www.theodinproject.com/ruby-on-rails/routing) and use it to <strong>answer the following questions</strong>
  1. What is the "Root" route? The "Root route tells rails wchich controller and action(methode inside the contoller) to map that that route to. 
  1. What are the seven RESTful routes for a resource? (1) GET all the posts.(2) GET just one specific post.(3) GET the page that lets you create a new post.(4) POST the data you just filled out for a new post back to the server so it can create that post.(5) GET the page that lets you edit an existing post (aka view the "edit post page).(6) PUT the data you just filled out to edit the post back to the server so it can perform the update.(7) DELETE on specific post by sending a delete request to the server.
  1. Which RESTful routes share the same URL but use different verbs? Routes (1) get,(4)post with the url "/posts/". Routes (2) get,(6) put,(7) delete with the url "/posts/:id".
  1. How do you specify an ID or other variable in a route? To specify an I or other variable in a route on will need to supply those to the hellper methods.
  1. How can you easily write all seven RESTful routes in Rails? 
      ...
      resources :posts
      ...
  1. What is the Rails helper method that creates the HTML for links? The 'link_to' Rails helper method creates the HTML for links.
1. Read the [Odin Project Controller Guide](http://www.theodinproject.com/ruby-on-rails/controllers)
1. Read the [Odin Project Views Guide](http://www.theodinproject.com/ruby-on-rails/views) and use it to <strong>answer the following questions</strong>
  1. What is a layout? Layouts are what contain <head> tags or the <DOCTYPE> declaration or some other basic structure that's present in all pages.
  1. What's the difference between a "view template" and a "layout"? View templatesis what is rendered form the controller and isn't the entire webpage. The layout contains the basic html elements that makes the structure of a basic webpage. 
  1. What is a "Preprocessor"? a preprocessor is a program that modifies data to conform with the inputs of another program. (ie ERB)
  1. Why are preprocessors useful? These are usefull because they are an easy way to implement multiple languages within one file while being very efficient.
  1. How do you make sure a preprocessor runs on your file? The file name must have the extension .erb. 
  1. What's the outputted filetype of a preprocessed *.html.erb file? What about a *.css.scss file?
  1. What is the difference between the <%= and <% tags? <% is used for purely code-related stuff like if statements and for loops, where you don't actually want anything displayed. Where as <%= outputts important peices of the instance variables that one has received from your controller.
  1. What is a view partial? These are HTML files that aren't meant to be complete but can be shared by other files.
  1. How do you insert a partial into your view? by adding the directory after a '#' symbol.
  1. How can you tell that a view file is a partial? with an underscore in front of the file. (ie _user_form.html.erb)
  1. How do you pass a local variable to a partial? To use the variable in your partial file, you drop the @ and call it like a normal variable
  1. What's the magical Rails shortcut for rendering a User? A bunch of Users? 
    A User 
        # app/views/index.html.erb
    <h1>Users</h1>
    <ul>
      <% @users.each do |user| %>
        <%= render user %>     
      <% end %>
    </ul>

    A bunch of users
    # app/views/index.html.erb
    <h1>Users</h1>
    <ul>
      <%= render @users %>
    </ul>
    
  1. What are asset tags and why are they used? Asset tags are helper methods that output HTML tags to grab CSS or Javascript files.
1. (By Monday 3/9) By yourself, complete the [Odin Project: Basic Routes, Views and Controllers](http://www.theodinproject.com/ruby-on-rails/basic-routes-views-and-controllers)
  1. Skip step 1 of the Application Skeleton section.  As we did last week, you will:
    1. Create a new Rails workspace on C9
    1. Add `/.c9` to your `.gitignore` file
    1. Setup git and commit the project:
      1. `git init`
      2. `git add .`
      3. `git commit -m 'initial commit'`
    1. Create a new repo on GitHub without a `README` or `.gitignore`
    1. Add your remote and push to github (replace the `<username>` and `<repo>` with your username and repo name)
      1. `git remote add origin https://github.com/<username>/<repo>.git`
      2. `git push -u origin master`
1. (By Thursday 3/12) As a group, complete the Rails tutorial [Chapter 5](https://www.railstutorial.org/book/filling_in_the_layout#top). Make sure to trade off coding, one person should not write everything.  
  1. Pick up where you left on your week 4 assignment with your new partner.  One person should be new to the codebase, one should have been working on it the previous week.

#### Optional
- Read the [Rails Guide on Routing](http://guides.rubyonrails.org/routing.html)
- Read the [Rails Guide on Controllers](http://guides.rubyonrails.org/action_controller_overview.html)
- Read the [Rails Guide on Layouts](http://guides.rubyonrails.org/layouts_and_rendering.html)
- Read the [Odin Project Guide on Asset Pipelines](http://www.theodinproject.com/ruby-on-rails/the-asset-pipeline)

# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
---------------------------------------------------------

Great Tutorial: https://www.youtube.com/watch?v=fmyvWz5TUWg

Process to create this project:
Install latest LTS version of Node.js
Install Yarn
Install Git-Bash
Install Sublime Text Editor
Install Windows Ruby 2.3 (railsinstaller.org - even though ruby is outdated - installs dependencies)
Install Ruby (rubyinstaller.org) (upgrades from ruby to 3+ from rails installer)

gitbash (ex: ruby -v) will show updated versions, however, rails will not be found
In gitbash type: gem install rails (this updates rails) (everything in ruby is gem based. It is a package (similar to pip in python)

mkdir /c/railsfriends (creates new dir)

rails new friends (creates new project)
ls (should show friends directory)
cd friends/ (should now show 'main' or 'master'
Open up Sublime text editor
Go to Project
Go to Add Folder To Project
Select c:/railsfriends/friendsIn Gitbash type: rails s (s stands for server)
Go to http://localhost:3000/
In another gitbash terminal : rails generate controller home index (or: rails g)

ex: create link: <%=link_to 'Friend List', root_path, class:"navbar-brand" %> config/routes.rb  root 'home#index'
friends/app/controllers - def index end


rails routes (shows all the routes in the app)

CREATE DB:
rails g scaffold friends first_name:string last_name:string email:string phone:string twitter:string (generates a scaffold/database table)
rails db:migrate (creates schema - creates db from migration

To install gem:add line to gem file
Terminal: bundle install

but...For Devise it's a little more complicated (instructions on homepage/github):

add to gem file
bundle install (installs items in gem file - much like requirements.txt in python)
rails generate devise:install (follow instructions -ex: copy items to file, 
rails g devise:views,
rails generate devise user(for db), rails db:migrate)
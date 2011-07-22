## Heroku-Backbone-Todo-App

This application shows how one can combine the usage of both [backbone.js](http://documentcloud.github.com/backbone/) on the client-side and [Ruby on Rails (3.0.7)](http://rubyonrails.org/) on the server-side with [Pusher](http://pusher.com) to create an rich interactive and collaborative application such as a todo-list manager.

This fork in particular is made to give you the fastest possible
deployment to heroku, so you can have your personal todo list app around
all the time.

## Code

The bulk of the application's front-end logic is heavily based off the [backbone.js todo-list example](http://documentcloud.github.com/backbone/docs/todos.html). We've written a small library that binds Pusher and Backbone together, the code to this can be found in [public/javascripts/backpusher.js](https://github.com/pusher/backbone-todo-app/blob/master/public/javascripts/backpusher.js). The usage of it can be seen in [public/javascripts/application.js](https://github.com/pusher/backbone-todo-app/blob/master/public/javascripts/application.js).

## Running on heroku

To get this application running on heroku, you should be able to simply clone this repository and run the following:

    gem install bundler
    bundle install
    heroku create
    git heroku push master
    heroku rake db:migrate
    open THE_WEBPAGE_YOU_GOT_FROM_HEROKU


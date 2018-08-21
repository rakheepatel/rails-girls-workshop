# Rails Girls Workshop

This project was created when I attended the Rails Girls workshop in August 2018 in Brisbane. Resources used were provided by [Ruby Girls Brisbane.](http://www.railsgirlsbne.com/guides-2017/)

Below are instructions on how to get this app running on your local OSX environment.

## Installing this app on your local
1. Clone this repo down, or fork it then clone it. Then `cd` into the project directory

2. I use [rbenv](https://github.com/rbenv/rbenv) to manage my Ruby versions. To install it use homebrew

    `brew install rbenv`

3. The app, at the time of writing, specifies ruby version 2.3.4, so use rbenv to install it

    `rbenv install 2.3.4`
 
4. Next we want to ensure our local ruby version is 2.3.4

    `rbenv local 2.3.4`
    
    If we check for `ruby --version` it should return `ruby 2.3.4.`

5. Because of the new ruby version we want to ensure our gems' version dependencies are correct. For that we need bundler

    `gem install bundler`

6. Bundler can now fix up our gem dependencies

    `bundle install`

    * Oh no! It fails! The gem "pg" (postgres) needs to be installed first with `brew install postgres` and then run `bundle install` again


7. The app contains two database gems now:

    * sqlite3 to run locally
    * pg to run on production

    There is also already a database in the app, so if you run `rails db:setup` it should fail saying a database already exists

8. Now we need to start the rails server to run the app

    `rails server`

    This should starts the server and specify a URL. Usually this would be `0.0.0.0:3000` or `localhost:3000`. If you go to this URL you should see your app running! :tada:

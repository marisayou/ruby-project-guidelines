# Flight Booker App

Created by[ Marisa You](https://github.com/marisayou), and [Rodrigo Rojas](https://github.com/crrojas88)

## Description

Flight Booker is a no frills CLI application used to find flights to your desired destinations. What Flight Booker lacks in niceties, it makes up for in functionality. 

This project is using Ruby and ActiveRecord, along with Sqlite3 for database management. Data is taken from the [SkyScanner API](https://skyscanner.github.io/slate/#api-documentation)

## Installation

Run bundle install to install the required gems.
```bash
bundle install
```

Type rake db:migrate in the terminal to run the migrations.
 
```bash
rake db:migrate
```

## To Run:

```bash
ruby bin/run.rb
```

## Usage

After running **ruby bin/run.rb**  in your terminal you will be prompted with a welcome menu.



If you do not have an account, you can choose _Sign up_ to create a username and password in order to be able to access your account as well as find and book flights.


After running bin/run.rb you will be prompted with the following welcome menu:

* Login
  - Login to your account with a username and password to access account menu.
* Sign up
  - Create an account with a username and password.
* Exit
  - Exit to terminal.

After creating an account and successfully signing in, you will be prompted with a list of options:


* View/Add Balance 
  - Views current balance / Adds desired amount to balance.
* Find and Book Flights 
  - Find and book a flight by inputting an Origin, Destination, and Date then choose which flight you’d like to book.
* View My Tickets 
  - Views current tickets held by that user.
* Logout 
  - Logs user out and returns to welcome menu.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

## Video

[Video presentation](https://youtu.be/gBlhx1FjNTM)




# Module One Final Project Guidelines

Congratulations, you're at the end of module one! You've worked crazy hard to get here and have learned a ton.

For your final project, we'll be building a Command Line database application.

## Project Requirements

### Option One - Data Analytics Project

1. Access a Sqlite3 Database using ActiveRecord.
2. You should have at minimum three models including one join model. This means you must have a many-to-many relationship.
3. You should seed your database using data that you collect either from a CSV, a website by scraping, or an API.
4. Your models should have methods that answer interesting questions about the data. For example, if you've collected info about movie reviews, what is the most popular movie? What movie has the most reviews?
5. You should provide a CLI to display the return values of your interesting methods.  
6. Use good OO design patterns. You should have separate classes for your models and CLI interface.

  **Resource:** [Easy Access APIs](https://github.com/learn-co-curriculum/easy-access-apis)

### Option Two - Command Line CRUD App

1. Access a Sqlite3 Database using ActiveRecord.
2. You should have a minimum of three models.
3. You should build out a CLI to give your user full CRUD ability for at least one of your resources. For example, build out a command line To-Do list. A user should be able to create a new to-do, see all todos, update a todo item, and delete a todo. Todos can be grouped into categories, so that a to-do has many categories and categories have many to-dos.
4. Use good OO design patterns. You should have separate classes for your models and CLI interface.

### Brainstorming and Proposing a Project Idea

Projects need to be approved prior to launching into them, so take some time to brainstorm project options that will fulfill the requirements above.  You must have a minimum of four [user stories](https://en.wikipedia.org/wiki/User_story) to help explain how a user will interact with your app.  A user story should follow the general structure of `"As a <role>, I want <goal/desire> so that <benefit>"`. For example, if we were creating an app to randomly choose nearby restaurants on Yelp, we might write:

* As a user, I want to be able to enter my name to retrieve my records
* As a user, I want to enter a location and be given a random nearby restaurant suggestion
* As a user, I should be able to reject a suggestion and not see that restaurant suggestion again
* As a user, I want to be able to save to and retrieve a list of favorite restaurant suggestions

## Instructions

1. Fork and clone this repository.
2. Build your application. Make sure to commit early and commit often. Commit messages should be meaningful (clearly describe what you're doing in the commit) and accurate (there should be nothing in the commit that doesn't match the description in the commit message). Good rule of thumb is to commit every 3-7 mins of actual coding time. Most of your commits should have under 15 lines of code and a 2 line commit is perfectly acceptable.
3. Make sure to create a good README.md with a short description, install instructions, a contributor's guide and a link to the license for your code.
4. Make sure your project checks off each of the above requirements.
5. Prepare a video demo (narration helps!) describing how a user would interact with your working project.
    * The video should:
      - Have an overview of your project. (2 minutes max)
6. Prepare a presentation to follow your video. (3 minutes max)
    * Your presentation should:
      - Describe something you struggled to build, and show us how you ultimately implemented it in your code.
      - Discuss 3 things you learned in the process of working on this project.
      - Address what, if anything, you would change or add to what you have today.
      - Present any code you would like to highlight.   
7. *OPTIONAL, BUT RECOMMENDED*: Write a blog post about the project and process.

---
### Common Questions:
- How do I turn off my SQL logger?
```ruby
# in config/environment.rb add this line:
ActiveRecord::Base.logger = nil
```

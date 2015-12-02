# ActiveRecord Models and Rails

## Objectives

1. Define ActiveRecord as the default ORM for rails
2. Build instance methods that extend a basic AR class
3. Create a migration by hand that inherits from AR:Migration and use correct naming for the file and class 
4. Use create_table
5. Create a model file by hand and inherit from AR
6. Use model conventions to correctly name the class based on the table name
7. Migrate the database with rake db:migrate
8. Access and write to a model from a Rails console
9. Read a model spec for an instance method
10. Describe how controllers and views have access to our model constant by convention and usage 
11. Read a database.yml and describe how it connects to different environment databases


## Notes

Build instance methods that extend a basic AR class (remind them that as a model AR classes interact with our database but can still function as normal classes and provide abstractions ontop of the data. They've done this previously in sinatra so they are familiar with AR)

AR models provide an abstraction for our database and persistance and lots of logic and functionality relating to the data our models provide to our application.

Our database might have a first_name and last_name column, which AR provides access to with first_name, and last_name readers/writers, but if we wanted to print a full_name, we'd build a full_name instance method that combines the first_name and last_name, so our models aren't just data, but also we build these sort of data helper methods.

First we need a table, so let's make a migration (they've done this before!)

001_create_posts.rb

we dont need to go too much into Migration syntax as they mostly learned this already or this readme can assume they are familiar with AR Basics such as migrations and stuff. but we'll have the migration code and link to migration docs for more information.

then we need a model file in app/models

post.rb

let's reiterate here convention over configuration, remind them of controller/action/view and now we have another one table/model/filename and migration_filename/migration_class

rake db:migrate (they know rake, and have done this)

accessing the model in rails console

reading a model spec. (first_name/full_name is a good example). They've done this a ton

explain models are separate from controllers and views - we connect a model to a controller and a view by loading the model in a controller action, no convention there...

database.yml defines are database connection and ActiveRecord::Base.connection holds those connections.

That's it for models in rails for now.

create a migration if needed, for new models for sure
define the model file, inherit from AR
use the model.
lets avoid generators for now....

<a href='https://learn.co/lessons/rails-activerecord-models-and-rails-readme' data-visibility='hidden'>View this lesson on Learn.co</a>

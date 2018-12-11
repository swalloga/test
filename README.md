# Databasic

### How to use:
* Clone this repo
* Run `bundle install`
* Run `rails db:create`
* Run `$ ruby databasic.rb`

### Summary:

Databasic is a lightweight Object-Relational Mapping tool that allows you to query and manipulate data from a database using an object-oriented paradigm, which I built to deepen my understanding of ActiveRecord.  

After spending years manipulating data in excel, I wanted to dive deeper into the connections between the object oriented models of Ruby and their corresponding tables in a SQL database.

### Usage:
Open database connection  
Run `rails db:create` to auto-generate a seeded database

Next, define a model to use the API methods.

The `foreign_key` for `has_many :pets` would have been defaulted to `:person_id` rather than `:owner_id`. This isn't the naming we want, so our associations allow overrides for `:class_name`, `:foreign_key`, and `:primary_key`. This is true for our `belongs_to` and `has_one_through` associations as well.

In this example, the table name `"persons"` will be inferred. To override the default, call `self.table_name = "new_name"`.

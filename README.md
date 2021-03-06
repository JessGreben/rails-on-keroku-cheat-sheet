## rails-on-heroku-cheat-sheet

### Generate New Rails app
    rails new app-name
    
### Rails Generate Examples
#### Create a Resource
    rails generate scaffold Post name:string title:string content:text
#### Generate Models
    rails generate model Post title:string body:text published:boolean
#### Add Column to Existing Model
    rails generate migration AddFieldToModel field:type
### Database Inital
#### Initial database setup
    rake db:setup
#### Update to Latest Migration
    rake db:migrate
#### Delete Database
    rake db:drop
#### Create Database
    rake db:create
#### Column Types
    :primary_key, :string, :text, :integer, :float, :decimal, :datetime, :timestamp, :time, :date, :binary, :boolean
### Database Maintenance
#### Reset database and reload current schema
    rake db:reset db:migrate
#### Destroy your db, create a new db and migrate current schema
    rake db:drop db:create db:migrate
#### Rails4, delete all contents on DB and recreate the schema from schema.rb file
    rake db:schema:load
    
### [Heroku](https://devcenter.heroku.com/articles/getting-started-with-rails5)
#### Create an app on Heroku
    heroku create
#### Deploy code 
    git push heroku master
#### Migrate the db
    heroku run rake db:migrate
#### Seed the db
    heroku run rake db:seed
#### Visit app in the browser
    heroku open
#### Visit logs
    heroku logs
    heroku logs --tail //full stream of logs
#### Rails console
    heroku run rails console
#### Set a config var on heroku
    heroku config:set VAR_NAME=value
#### See what config vars are available
    heroku config

# Heroku Postgres - database on demand 
  
  Postgres is a very impressive database with a very wide range of features, its also a very active open source project with a long history.  [Heroku Postres](https://www.heroku.com/postgres) has wrapped the same kind of developer focused services around Postgres to make it really easy to use.

![Heroku Postgres features](../images/heroku-postgres-features-concept.png)
  
  With [Heroku Postgres](https://www.heroku.com/postgres) you can provision a database instantly, just like you can with any other addon service.

  When deploying Java applications, a Postgres database is automatically added.  So in your sample application you can see Heroku Postgres as an addon that is aready provisioned.

> **Comment** [Heroku Postress](http://postgres.heroku.com/) can be added to your Herokup application or run as a standalone database.
  

### Working with Postress

  Postgres can be used from you application just like any other database.  So you specify a driver and add code to your app to query the database.
  
  Heroku provides you with the database connection details in a configuration variable called DATABASE_CONFIG.  You can also see details of your database from the Heroku dashboard or via the Heroku command line.
  
  You can also use the Heroku connection details to connect your own database clients.


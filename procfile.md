Avoid hardcoded Configuration

>TODO: This section is probably hideously out of date


> NOTE: Where ever possible, put all configuration values in the Heroku Config Variables, its much more secure and far less prone to human error.  Heroku Configuration Variables also provide a much simpler way to use different configuration settings across environments (eg. dev, test, staging, production) 

---

##  Procfile changes  
  In the Procfile we can set up all sorts of parameters to define how Heroku runs our apps.  Common paramters include ports, memory heap sizes and data sources.
  
  Using system properties for the database we override the application configuration when running on Heroku.  

  Create a Procfile for Heroku in the root application directory containing the following:

    web: target/start -Dhttp.port=${PORT} -DapplyEvolutions.default=true -Ddb.default.url=${DATABASE_URL} -Ddb.default.driver=org.postgresql.Driver

  Or you can just download [a ready made Procfile](resources/Procfile) if you prefer.

  Note: Read more about [Deploying Play apps to Heroku](http://www.playframework.com/documentation/2.1.0/ProductionHeroku).


## Commit your changes locally and deploy

  Again as we have made a significant change to the web app functionality, even though its not complete, we should commit those changes to Git.
  
  Add these changes to your local git repository as follows:
  
    git add .
    git commit -m "Added Postgres dependencies and Procfile"

  Push this commit to Heroku to deploy the new version of the code using the command
  
    git push heroku master

  Reload your browser to check the live website has been updated, or use the command `heroku open`  

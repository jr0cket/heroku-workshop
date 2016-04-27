# The Heroku Procfile 
  
  A Procfile is a simple text file that lists all the process types that make up an application. Each process type is a declaration of a command that is executed when a dyno of that process type is started.

> **Comment** The Procfile is the only Heroku specific file you add to your project in order to run your application on Heroku.

The syntax of the Procfile is as follows:

  * `process type` – the process type for your command.  If the process type is `web` then the process will listen to web traffic.  Any other name is considered a background task, often used for longer running tasks or processing queues.
  
  * `command` – the command to launch the process, as would be run on the command line.

### Example Procfile 

  In the sample Java application that we have worked with, the contents of the Procfile is as follows:

```
web: java -cp target/classes:target/dependency/* Main
```

  As our application is a website, the first part of this line is the process type `web` so it will listen to web requests.
  
  The process type is followed by the command to run your application.  As this is a Java application, its a standard `java` command that sets the classpath `-cp` and states the entry point class run.

> **Comment** You can reference configuration variables added to your Heroku app, the most commonly used being the $PORT variable.  

> As Heroku automatically reassigns the actual port your application listens on, if your application configuration needs a port number you should use $PORT instead.  Heroku sets the $PORT value every time a new dyno is created.


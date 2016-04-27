# The Process model

  We have discussed previously how Heroku uses a dyno model so you do not need to deal with all the complexities of a server.  A dyno is a container that runs a single application processes.  The process types are defined in a simple text file called **Procfile** in the root of your project.
  
  Each of the process defined in your Procfile will run on its own dyno.  When you scale, you increase the number of dyno's running that process.


### Processes types

  There are two process types you can define: **web** and _anything else_.

#### Web process types  

  A web process listens to requests and responds with results, just as a web server or application server would.

  All request sent to your application are routed through to the dyno's you have running.  So the more dynos you run, the more requests you application can process.  


#### Common names for other process types

* `Worker` - a generic name for a background task.

* `Queue` - a process that consumes data from a queue service attached to the application.  Typically data is passed to the queue from a web process, so that process does not have to perform any long operation or extended wait.

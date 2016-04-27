# One-off tasks 

  You can run a one-off task in two ways.  You can either run a shell remotely and then run a command, or you can run the command all in one go.
  
    heroku run bash
    heroku run <command>
 
  A newly provisioned dyno is provisioned with the latest version of your application running on it.  Therefore any process that is part of your application can be run.  

#### Running a remote shell

> **Note** run a one-time task by connecting to a new dyno in your application 

  Using the Heroku toolbelt, run the command 

    heroku run bash  

  This command opens a shell in a complete copy of your running application and you work with the application and file space as you would on any Linux server.  Not all the tools common to a Linux server are available.
   In the shell of your application, run commands such as `ls` and `cd` to explore the filespace that makes up your application.
   
    ls 
    cd <directory>
    mkdir <directory>
    rm -r <directory>
    ps ax
    top
    exit

  Terminate by the remote shell session with the `exit` command or pressing `Ctrl-C`. 
  
> **Hint**  See the [online manual pages for Unix systems](https://www.kernel.org/doc/man-pages/) to see what commands do and the options you can use with a command.
  
---

#### Running a command 

  Here are some examples of running commands directly 

    heroku run "java -jar db-migrate.jar"
    heroku run "rake db:migrate"    
    heroku run "node migrate.js migrate"
    
  You could also connect to a language or framework run time environment (eg. a REPL)

    heroku run "rails console"
    heroku run "irb"
    heroku run "node"
    heroku run "lein repl"
    heroku run "sbt"
    heroku run "play"

#### Logging one-time processes 

  One-off dynos are named in the log as `run.X`
  
```
$ heroku ps
=== run: one-off processes
run.7364: starting 2013/03/13 15:38:08 (~ 1s ago): `bash`
```
 
> **Comment** As `STDOUT` is sent to your terminal, the only thing logged is the startup & shutdown of the dyno running the one-off task.

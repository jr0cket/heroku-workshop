# Rolling back a release 

  It happens to us all, we push a change and there is some bug that causes issues with our app despite all our testing.  Rather than leave a buggy application running, with Heroku you can instantly rollback to a previous release and give yourself more time to investigate the root cause of the issue.
  
  You can see all the releases you have done for your app in the Heroku Dashbaord.
  
  ![Heroku Dashboard app releases]()
  
  You can also select a previous release to roll back to.
  
  ![Heroku Dashboard release rollback]()
  
---

  You can also use the Heroku Toolbelt to list the releases and roll back to any of the previous releases.
  
    heroku releases 
    heroku rollback v21

> TODO: screenshots of output, check command syntax

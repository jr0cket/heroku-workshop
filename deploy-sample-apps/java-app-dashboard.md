# Dashboard view of the sample Java app

> **Note** Open your Heroku dashboard in a browser by visiting [www.heroku.com](https://www.heroku.com) and logging in.  If you are already logged in when you visit [www.heroku.com](https://www.heroku.com) you are automatically re-directed to the dashboard.

  View the dashboard of the application you just deployed by clicking on its name.  If you have many applications on your Heroku account, you can also use the search bar at the top to filter the list of apps in the list.

  You should see the resources tab of your newly deployed application.  This shows you how many resources you are using for your app (1 dyno) and how much it is costing you a month currently (zero $).
  
![Heroku sample app java - dashboard resources](../images/heroku-app-sample-java-dashboard-resources.png)
 
  Click on the **Activity** tab to see everything that has happend regarding this app on Heroku.  
  
  The first two entries are the initial release and logging service being added, triggered  when you ran the `heroku create` command.  The rest of the activity items were triggered by the `git push` deployment.  They include building the code, attaching a database, setting a database config variable, setting Path & Java config variables and the final release of the app.

![Heroku sample app java - dashboard activity](../images/heroku-app-sample-java-dashboard-activity.png)

  Each build item in the activity feed has a link to view the log for that build.  As a built can output many lines of text during a deployment, the build log is a convienient way to review any issues that may have occured during the build.
  
![Heroku sample app java - dashboard activity build log](../images/heroku-app-sample-java-dashboard-activity-build-log.png)

  Click on the **Settings** tab to see infomation about your Heroku app.  
  
  Here you can see the region your application is deployed in, either US for the east coast USA data center or EU for the European data center in Ireland.  You can see the stack your app is running on, essentially the Heroku Operating System and associated infrastructure.
  
  Its important to keep an eye on the slug size of your application, as there are slug size [limits](https://devcenter.heroku.com/articles/slug-compiler#slug-size) (300MB max) and the bigger the slug the longer your build is likely to take.

![Heroku sample app java - dashboard ](../images/heroku-app-sample-java-dashboard-settings-info.png)

  You can see and edit the Configuration Variables for you Heroku app.

![Heroku sample app java - dashboard ](../images/heroku-app-sample-java-dashboard-settings-config-variables.png)

  You can also do other actions such as delete, rename, transfer ownership of your Heroku app.
 
![Heroku sample app java - dashboard ](../images/heroku-app-sample-java-dashboard-settings-domain-ownership-delete.png)

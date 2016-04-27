# Scheduling Tasks

  Sometimes you want to run a task or script just once rather than continually running.  Heroku provides several ways to do this.

#### Scheduled tasks 

Regular short running tasks can be managed via the [Heroku Scheduler](https://addons.heroku.com/scheduler) or [Temoporise Scheduler](https://addons.heroku.com/temporize) addons.  These services allow you to configure CRON-like regular tasks from executable processes deployed along with you application

#### Longer running tasks 
 
  Longer running tasks can be run using a dyno process running in the background.  This dyno type is usually called a `worker` dyno, although you can call it anything you like.
  
  Background jobs help you build scalable web apps as they can process both time and compute intensive tasks.  This helps ensure that web requests always return under the reccommended 500ms response time.
  
  Typical activities of a `worker` dyno include Fetching data from remote APIs, reading RSS feeds, resizing images and uploading data to longer term storage (eg. Amazon S3 buckets).
  
#### One-off tasks

One-time tasks can be run using the Heroku toolbelt command `heroku run <command>`.  These tasks are run in their own isolated dyno, an exact copy of your currently running application.

> **Comment** You can only change your applicaiton in production via a push of the codebase or changing configuration variables.  Connecting directly to your live environments can lead to only fixing an issue in production and not in the codebase.

  You can run one-time tasks with more resources by specifying the size of dyno they run upon

```
    heroku run --size=2X <command>
    heroku run --size=PX <command>
```



